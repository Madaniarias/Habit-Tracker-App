# PYTHON CODE FOR HABIT TRACKER PROJECT

```.py
from kivymd.app import MDApp
from kivymd.uix.datatables import MDDataTable
from kivymd.uix.dialog import MDDialog
from kivymd.uix.pickers import MDDatePicker
from kivymd.uix.screen import MDScreen
import sqlite3
from secure_password import encrypt_password, check_password, pwd_config


# Creating class data_base handler
class database_handler:

    # initialize values
    def __init__(self, namedb: str):
        self.connection = sqlite3.connect(namedb)
        self.cursor = self.connection.cursor()

    def search(self, query):
        result = self.cursor.execute(query).fetchall()
        return result

    def run_save(self, query):
        self.cursor.execute(query)
        self.connection.commit()

    # creating query that created table if not exits.
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
        # run the query
        self.run_query(query1)
        self.run_query(query2)

    # run query
    def run_query(self, query: str):
        self.cursor.execute(query)
        self.connection.commit()

    # close connection
    def close(self):
        self.connection.close()


# Create class LoginScreen
class LoginScreen(MDScreen):

    # Used for to confimr the information when the user logs in
    def try_login(self):
        # define local variables
        email = self.ids.email.text
        passwd = self.ids.passwd.text

        # connect to database
        db = database_handler(namedb="habit_tracker.db")

        # creat query to get id, password from the table user where the email is the same
        query = f"SELECT id, password FROM user WHERE email = '{email}'"

        # execute query
        result = db.search(query)

        # if result variable is not empty, identify hashed password. If password by user matches hash continue
        if result and pwd_config.identify(result[0][1]) and check_password(hashed=result[0][1], user_password=passwd):
            user_id = result[0][0]  # Get the user ID from the database
            # print in the terminal to check if it is working
            print(f"Login successful")
            # access user id from Main Screen
            self.parent.get_screen(
                'MainScreen').user_id = user_id  # Set the user ID as an attribute of the MainScreen instance
            # Go to Main Screen
            self.parent.current = "MainScreen"
            self.ids.email.text = ""
            self.ids.passwd.text = ""

        # if email has 0 characters and password has 0 characters print error
        elif len(email) == 0 and len(passwd) == 0:
            print("Incorrect email or password")
            self.ids.email.error = True
            self.ids.passwd.error = True
            self.ids.email.helper_text = "This field is required."
            self.ids.passwd.helper_text = "This field is required."
            dialog = MDDialog(title="Seems like something went wrong. Try again")
            dialog.open()

        # else show error
        else:
            print("Incorrect email or password")
            self.ids.email.error = True
            self.ids.passwd.error = True
            self.ids.email.helper_text = "Incorrect email or password"
            self.ids.passwd.helper_text = "Incorrect email or password"
            dialog = MDDialog(title="Seems like something went wrong. Try again")
            dialog.open()


# Create class RegistrationScreen
class RegistrationScreen(MDScreen):

    # For when user tries to register a new acc
    def try_register(self):

        # define local variables
        uname = self.ids.uname.text
        email = self.ids.email.text
        passwd = self.ids.passwd.text
        passwd_check = self.ids.passwd_check.text

        # Username policy
        # If username has 0 characters or space, show error
        if len(uname) == 0 or " " in uname:
            if len(uname) == 0:
                self.ids.uname.error = True
                self.ids.uname.helper_text = "This field is required."
            if " " in uname:
                self.ids.uname.error = True
                self.ids.uname.helper_text = "Username should not contain spaces."
            return

        # Email policy
        # If email does not have @, has 0 characters or already exists in database, show error
        if "@" not in email or len(email) == 0 or database_handler("habit_tracker.db").search(
                f"SELECT * FROM user WHERE email = '{email}'"):
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

        # Password policy
        # If username has 0 characters, space, is not equal to passw check or has less tha 4 charc, show error
        if len(passwd) < 4 or " " in passwd or passwd != passwd_check or len(passwd) == 0:
            if len(passwd) < 4:
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
            return

        # Password check policy
        # If check password has 0 characters, show error
        if len(passwd_check) == 0:
            self.ids.passwd_check.error = True
            self.ids.passwd_check.helper_text = "This field is required."
            return

        # when password matches
        else:
            # hash the password
            hash = encrypt_password(passwd)

            # Connect to database
            db = database_handler(namedb="habit_tracker.db")

            # Create query to insert new info in user table in database
            query = f"INSERT into user (email,password,username) values('{email}','{hash}','{uname}')"
            db.run_save(query)
            db.close()

            # print to check what is happening
            print("Registration completed")

            # Return to Login Screen
            self.parent.current = "LoginScreen"

            # Show message to user
            dialog = MDDialog(title="Your registration was successful! WELCOME!",
                              md_bg_color="#eededc"
                              )
            dialog.open()
            self.ids.uname.text = ""
            self.ids.email.text = ""
            self.ids.passwd.text = ""
            self.ids.passwd_check.text = ""

            return


# Create class Main Screen
class MainScreen(MDScreen):
    # define local variables
    checks = [0, 0, 0, 0, 0]
    progress_amount = 0

    # initialize
    def __init__(self, *args, **kwargs):
        super().__init__(*args, **kwargs)
        self.selected_date = None

    # date selector
    def date(self):
        date_dialog = MDDatePicker()
        date_dialog.bind(on_save=self.on_save)
        date_dialog.open()

    # saving date selected
    def on_save(self, instance, value, data_range):
        self.selected_date = value
        self.ids.progress_date.text = f"{value}"

    # connecting checkboxes to percentage
    def checkbox_click(self, value, habits):
        self.checks[habits - 1] = int(value)
        if value:
            self.progress_amount += 20
        else:
            self.progress_amount -= 20

        # displaying percentage
        self.ids.progressbar.value = self.progress_amount
        self.ids.percent_label.text = f"{self.progress_amount}%"

    # saving habit progress to database
    def save(self):
        # make user specific (only show relevant info to current user)
        user_id = self.parent.get_screen('MainScreen').user_id  # Retrieve the user ID from the MainScreen instance
        habit1 = MainScreen.checks[0]
        habit2 = MainScreen.checks[1]
        habit3 = MainScreen.checks[2]
        habit4 = MainScreen.checks[3]
        habit5 = MainScreen.checks[4]

        progress_date = self.parent.get_screen(
            'MainScreen').selected_date  # Retrieve the progress_date value from the MainScreen instance
        percentage = self.parent.get_screen('MainScreen').progress_amount

        # make so progress cant be saved twice for same day
        if database_handler("habit_tracker.db").search(f"SELECT * FROM habit WHERE progress_date = '{progress_date}'"):
            self.ids.save_button.error = True
            self.ids.error_text.text = "*Progress for the day already registered."

        # save progress into habit table in database
        else:
            db = database_handler("habit_tracker.db")
            query = f"INSERT INTO habit(user_id, habit1,habit2,habit3,habit4,habit5, percentage, progress_date) VALUES ('{user_id}','{habit1}', '{habit2}', '{habit3}', '{habit4}', '{habit5}', '{percentage}','{progress_date}')"
            db.run_save(query)
            db.close()

            # Show message to user
            dialog = MDDialog(title="Congrats you updated your progress!")
            dialog.open()


# Create HistoryScreen
class HistoryScreen(MDScreen):
    data_table = None

    # Creating table display for habit history
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

        # checkbox selection
        self.data_table.bind(on_row_press=self.row_pressed)
        self.data_table.bind(on_check_press=self.check_pressed)
        self.add_widget(self.data_table)  # add table to th GUI

        # update table
        self.update()

    def row_pressed(self, table, row):
        print("a row was pressed", row.text)

    def check_pressed(self, table, current_row):
        print("a check mark was pressed", current_row)

    # Delete row selected when history table is displayed
    def delete(self):
        checked_rows = self.data_table.get_row_checks()
        db = database_handler("habit_tracker.db")

        # for the checked rows
        for r in checked_rows:
            id = r[0]

            # query to delete
            query = f"delete from habit where id_habit={id}"
            db.run_save(query)
        db.close()

        # update table
        self.update()

    # update info
    def update(self):
        # make user specific
        user_id = self.parent.get_screen('MainScreen').user_id
        # read database
        query = f"SELECT * FROM habit WHERE user_id={user_id}"
        db = database_handler("habit_tracker.db")
        data = db.search(query)
        db.close()
        self.data_table.update_row_data(None, data)


# Create class habit_kivy to read kivy file
class habit_kivy(MDApp):

    # build screen
    def build(self):
        return


# Create an object
db = database_handler(namedb="habit_tracker.db")
db.create_tables()
db.close()
test1 = habit_kivy()
test1.run()
```
