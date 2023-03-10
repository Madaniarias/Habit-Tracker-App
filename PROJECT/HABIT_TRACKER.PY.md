# PYTHON CODE FOR HABIT TRACKER PROJECT

```.py
from kivymd.app import MDApp
from kivymd.uix.datatables import MDDataTable
from kivymd.uix.dialog import MDDialog
from kivymd.uix.pickers import MDDatePicker
from kivymd.uix.screen import MDScreen
import sqlite3
from secure_password import encrypt_password, check_password, pwd_config


class database_handler:

    def __init__(self, namedb: str):
        self.connection = sqlite3.connect(namedb)
        self.cursor = self.connection.cursor()

    def search(self, query):
        result = self.cursor.execute(query).fetchall()
        return result

    def run_save(self, query):
        self.cursor.execute(query)
        self.connection.commit()

    def create_tables(self):
        query1 = f"""CREATE TABLE if not exists user(
            id INTEGER PRIMARY KEY,
            username text NOT NULL,
            email text NOT NULL,
            password text NOT NULL
        )"""
        query2 = f"""CREATE TABLE if not exists habit(
            id_habit INTEGER PRIMARY KEY,
            user_id INTEGER NOT NULL,
            habit1 INTEGER NOT NULL,
            habit2 INTEGER NOT NULL,
            habit3 INTEGER NOT NULL,
            habit4 INTEGER NOT NULL,
            habit5 INTEGER NOT NULL,
            percentage INTEGER NOT NULL,
            progress_date TEXT NOT NULL UNIQUE
        )"""
        self.run_query(query1)
        self.run_query(query2)

    def run_query(self, query: str):
        self.cursor.execute(query)
        self.connection.commit()

    def close(self):
        self.connection.close()


class LoginScreen(MDScreen):

    def try_login(self):

        email = self.ids.email.text
        passwd = self.ids.passwd.text

        db = database_handler(namedb="habit_tracker.db")
        query = f"SELECT id, password FROM user WHERE email = '{email}'"
        result = db.search(query)


        if result and pwd_config.identify(result[0][1]) and check_password(hashed=result[0][1], user_password=passwd):
            user_id = result[0][0]  # Get the user ID from the database
            print(f"Login successful")
            self.parent.get_screen(
                'MainScreen').user_id = user_id  # Set the user ID as an attribute of the MainScreen instance
            self.parent.current = "MainScreen"
            self.ids.email.text = ""
            self.ids.passwd.text = ""

        elif len(email) == 0 and len(passwd) == 0:
            print("Incorrect email or password")
            self.ids.email.error = True
            self.ids.passwd.error = True
            self.ids.email.helper_text = "This field is required."
            self.ids.passwd.helper_text = "This field is required."
            dialog = MDDialog(title="Seems like something went wrong. Try again")
            dialog.open()

        else:
            print("Incorrect email or password")
            self.ids.email.error = True
            self.ids.passwd.error = True
            self.ids.email.helper_text = "Incorrect email or password"
            self.ids.passwd.helper_text = "Incorrect email or password"
            dialog = MDDialog(title="Seems like something went wrong. Try again")
            dialog.open()




class RegistrationScreen(MDScreen):
    def try_register(self):

        uname = self.ids.uname.text
        email = self.ids.email.text
        passwd = self.ids.passwd.text
        passwd_check = self.ids.passwd_check.text

        if len(uname) == 0 or " " in uname:
            if len(uname) == 0:
                self.ids.uname.error = True
                self.ids.uname.helper_text = "This field is required."
            if " " in uname:
                self.ids.uname.error = True
                self.ids.uname.helper_text = "Username should not contain spaces."
            return

        if "@" not in email or len(email) == 0 or database_handler("habit_tracker.db").search(f"SELECT * FROM user WHERE email = '{email}'"):
            if "@" not in email:
                self.ids.email.error = True
                self.ids.email.helper_text = "Invalid email. Needs to include @ sign."
            if len(email) == 0:
                self.ids.email.error = True
                self.ids.email.helper_text = "This field is required."
            if database_handler("habit_tracker.db").search(
                    f"SELECT * FROM user WHERE email = '{email}'"):
                self.ids.email.error = True
                self.ids.email.helper_text = "A user already exists with this email."
            return


        if len(passwd) < 4 or " " in passwd or passwd != passwd_check or len(passwd) == 0:
            if len(passwd) < 8:
                self.ids.passwd.error = True
                self.ids.passwd.helper_text = "Password must be longer than 4 characters."
            if " " in passwd:
                self.ids.passwd.error = True
                self.ids.passwd.helper_text = "Password cannot contain spaces."
            if passwd != passwd_check:
                self.ids.passwd_check.error = True
                self.ids.passwd.error = True
                self.ids.passwd_check.helper_text = "Passwords do not match."
                self.ids.passwd.helper_text = "Passwords do not match."
            if len(passwd) == 0:
                self.ids.passwd.error = True
                self.ids.passwd.helper_text = "This field is required."

        if len(passwd_check) == 0:
            self.ids.passwd_check.error = True
            self.ids.passwd_check.helper_text = "This field is required."
            return


        else:  # password match
            # hash the password
            hash = encrypt_password(passwd)
            db = database_handler(namedb="habit_tracker.db")
            query = f"INSERT into user (email,password,username) values('{email}','{hash}','{uname}')"
            db.run_save(query)
            db.close()
            print("Registration completed")
            self.parent.current = "LoginScreen"
            dialog = MDDialog(title="Your registration was successful! WELCOME!",
                              md_bg_color="#eededc"
                              )
            dialog.open()
            self.ids.uname.text = ""
            self.ids.email.text = ""
            self.ids.passwd.text = ""
            self.ids.passwd_check.text = ""

            return

class MainScreen(MDScreen):
    checks = [0, 0, 0, 0, 0]
    progress_amount = 0

    def __init__(self, *args, **kwargs):
        super().__init__(*args, **kwargs)
        self.selected_date = None

    def date(self):
        date_dialog = MDDatePicker()
        date_dialog.bind(on_save=self.on_save)
        date_dialog.open()

    def on_save(self, instance, value, data_range):
        self.selected_date = value
        self.ids.progress_date.text = f"{value}"

    def checkbox_click(self, value, habits):
        self.checks[habits - 1] = int(value)
        if value:
            self.progress_amount += 20
        else:
            self.progress_amount -= 20

        self.ids.progressbar.value = self.progress_amount
        self.ids.percent_label.text = f"{self.progress_amount}%"


    def save(self):
        user_id = self.parent.get_screen('MainScreen').user_id  # Retrieve the user ID from the MainScreen instance
        habit1 = MainScreen.checks[0]
        habit2 = MainScreen.checks[1]
        habit3 = MainScreen.checks[2]
        habit4 = MainScreen.checks[3]
        habit5 = MainScreen.checks[4]

        progress_date = self.parent.get_screen(
            'MainScreen').selected_date  # Retrieve the progress_date value from the MainScreen instance
        percentage = self.parent.get_screen('MainScreen').progress_amount

        if database_handler("habit_tracker.db").search(f"SELECT * FROM habit WHERE progress_date = '{progress_date}'"):
            self.ids.save_button.error = True
            self.ids.error_text.text = "*Progress for the day already registered."

        else:
            db = database_handler("habit_tracker.db")
            query = f"INSERT INTO habit(user_id, habit1,habit2,habit3,habit4,habit5, percentage, progress_date) VALUES ('{user_id}','{habit1}', '{habit2}', '{habit3}', '{habit4}', '{habit5}', '{percentage}','{progress_date}')"
            db.run_save(query)
            db.close()
            dialog = MDDialog(title="Congrats you updated your progress!")
            dialog.open()

class HistoryScreen(MDScreen):
    data_table = None

    def on_pre_enter(self, *args):
        # Before the screen is created, this code is run
        self.data_table = MDDataTable(
            size_hint=(.8, .5),
            pos_hint={"center_x": .5, "center_y": .5},
            use_pagination=True,
            check=True,
            # title for the coluns
            column_data=[("ID on system", 35),
                         ("User ID", 20),
                         ("Study Math", 23),
                         ("Go to gym", 23),
                         ("Study CS", 23),
                         ("Sleep 8 hours", 25),
                         ("Make bed", 22),
                         ("PERCENTAGE", 23),
                         ("PROGRESS DATE", 25)
                         ]
        )

        self.data_table.bind(on_row_press=self.row_pressed)
        self.data_table.bind(on_check_press=self.check_pressed)
        self.add_widget(self.data_table)  # add table to th GUI

        self.update()

    def row_pressed(self, table, row):
        print("a row was pressed", row.text)

    def check_pressed(self, table, current_row):
        print("a check mark was pressed", current_row)

    def delete(self):
        checked_rows = self.data_table.get_row_checks()
        db = database_handler("habit_tracker.db")
        for r in checked_rows:
            id = r[0]
            query = f"delete from habit where id_habit={id}"
            db.run_save(query)
        db.close()
        self.update()

    def update(self):
        user_id = self.parent.get_screen('MainScreen').user_id
        # read database
        query = f"SELECT * FROM habit WHERE user_id={user_id}"
        db = database_handler("habit_tracker.db")
        data = db.search(query)
        db.close()
        self.data_table.update_row_data(None, data)


class habit_kivy(MDApp):

    def build(self):
        return


# Create an object
db = database_handler(namedb="habit_tracker.db")
db.create_tables()
db.close()
test1 = habit_kivy()
test1.run()

```
