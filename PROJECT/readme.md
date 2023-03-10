![habitmainread](https://user-images.githubusercontent.com/111761417/218357449-7073b4e8-d717-4513-a9fa-abf59a054408.gif)
# UNIT 3: A HABIT TRACKER FOR MS. LISON HEBERT.

**Table of Contents**
1. [Criteria A: Planning](#criteria-a-planning)
   * [Problem definition](#problem-definition)
   * [Rationale for Proposed Solution](#rationale-for-proposed-solution)
   * [Design statement](#design-statement)
   * [Success Criteria](#success-criteria)
2. [Criteria B: Design](#criteria-b-design)
    * [Record of Tasks](#record-of-tasks)
    * [System diagram](#system-diagram)
    * [Wireframe](#wireframe)
    * [Flow Diagrams](#flow-diagrams)
    * [ER Diagrams](#er-diagrams)
    * [UML Diagrams](#uml-diagrams)
    * [Test Plan](#test-plan)
3. [Criteria C: Development](#criteria-c-development)
   * [Existing Tools](#existing-tools)
   * [Techniques Applied](#techniques-applied)
   * [Computational Thinking](#computational-thinking)
4. [Criteria D: Functionality](#criteria-d-functionality)
   * [Sources](#sources)

## Criteria A: Planning

## Problem definition

A highschool student, Lison Hebert, is interested in building good habits to improve her daily rutine and help her reach your goals. She has been manually keeping track of her habit completion in a personal diary, however at the moment this method has become too time consuming and tedious to keep track off. It is also difficult for the highschool student to see the progresss in an organized manner. The client is in need of a habit tracker application that helps her visualize, organize and keep track of her progress in the course of developing good habits. Additional, it si important to consider that the client's budget is limited.

## Rationale for Proposed Solution

Considering the client requirements an adequate solution includes a habit tracker application that helps her visualize, organize and keep track of her progress in the course of developing good habits. For this application it may adequate to consider a computer program with a GUI (Graphical User Interface) that can store data into a database. Considering the budgetary constrains of the client, the software tool that I proposed for this solution is Python. Python is free and platform-independent. That is, if you write the code on one of the Windows, Mac, or Linux operating systems, then you can run the same code on the other OS with no need for any changes so it can be run. In other words, it can be supported by multiple platforms. Nevertheless, requieres a lot of memeory[^1]. Regarding data storage for this solution, SQLite can be a good option. SQLite is the most used database engine in the world. SQLite is built into all mobile phones and most computers and comes bundled inside countless other applications that people use every day. The code for SQLite is in the public domain and is thus free for use for any purpose, commercial or private[^2]. A database engine is the software that does the real work of sorting the information, finding specific data that you request, and so on [^3]. This makes it a good option for the proposed solution as the habit tracker will be displaying, storing and deleting data regarding th habits of the client. As for the GUI (Graphical User Interface), KivyMD is good option to consider. A graphical user interface (GUI) is an interface through which a user interacts with electronic devices such as computers and smartphones through the use of icons, menus and other visual indicators or representations (graphics) [^4]. This GUI tool is very simple and allows to create the displays required by the proposed solution.

## Design statement

I will design and make a habit tracker application for a highschool student. The project will be about designing that helps her visualize, organize and keep track of her progress in the course of developing good habits and will be constructed using the software Python 3.10.7, SQLite (database engine) and KivyMD (Graphical User Interface tool). It will take about 4 weeks to make and will be evaluated according to the criteria below.

## Success Criteria

1. The solution provides a login screen that uses email and is protected by password. Also, povides a registration screen that requests username, email, password and checks the password.
2. The solution will display the history of all habits. It will show the completion of each individual habit and the overall completionn of habits of a particular day.
3. The solution provides a tracking system for up 5 to habits.
4. The solution allows the user to save habits completion per day and displays the progress in a graphic manner.
5. The solution allows the user to delete saved habit information from the history of all habits.
6. The solution should have a function to stop from saving habit progress twice the same day.

Color palette provided:

![IMG_0177](https://user-images.githubusercontent.com/111761417/223729114-8eedd061-e2ed-427f-9e90-f4e64055604b.jpg)

# Criteria B: Design

## Record of Tasks
| Task No | Planned Action                                                | Planned Outcome                                                                                                 | Time estimate | Target completion date | Criterion |
|---------|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|---------------|------------------------|-----------|
| 1      | Planning: First meeting with client |  Getting a sense of what is the problem and the needs of the client. Start to get a deeper understanding of how does the desire interface looks for the client. Note taking on the meeting  | 6min                  | Feb 9 | A
| 2      | Analysis of planning meeting | Taking information learnt form the first meeting with the client to see what was understood from the developer part and present next meeting with client to confirm if the information was understood correctly. |  10 min  | Feb 9 | A
| 3      | Planning: Second meeting with client | Getting a sense of what is the problem and the needs ofthe client. Go together through the information again and understand can be made and what cannot. Note taking on the meeting | 5 min | Feb 21 | A
| 4      | Analysis of planning meeting | Taking information learnt form the second meeting with the client to see what was understood from the developer part and present next meeting with client to confirm if the information was understood correctly. | 15 min | Feb 21 | A
| 5      | Problem definition | After the meetings with the client, establish the problem that the project is going to be solving specifically and what are the main needs of the client | 20 min | Feb 23 | A
| 6      | Planning: Establishing Success criteria | Taking into account the problem definition previously established, meet with the client once again to establish the success criteria for the habit tracker. Establish where the primary focus should be when developing th application to satisfy the client's neccesities | 10 min | Feb 23 | A
| 7      | Approval of Success Criteria by Client | After meeting with the client, sent a finalized version of the succes criteria and got approval of the 6 succes criteria by the client | 20 min | Feb 23 | A 
| 8      | Design statement | taking into account the previously approved succes criteria and problem definition, explain in a consice and clear manner the purpose of the project to the client | 5 min | Feb 23 | A
| 9      | Rationale for Proposed Solution | Analize the design statement, success criteria and client's needs and determine which tools best suit the development of the habit tracker application  | 20 min | Feb 23 | A
| 10     | System Diagram | Draw the system diagram for the habit tracker to have a clear idea of the hardware and software requirements for the proposed solution. | 30 min | March 1 |  B
| 11     | Wireframe | Draw the wireframe for the habit tracker to have a clear idea of the design of the screens and functionality for the proposed solution. | 45 min | March 1 |  B
| 12     | Planning: Design approval by client | Meet with client and show and explain wireframa diagram and got approval for the habit tracker application design | 30 min | March 2 | B
| 13     | ER Diagrams | Draw the ER Diagram for the habit tracker application to have a clear idea of the tables needed in the database for the proposed solution. | 10 min | March 2 | B
| 14     | Create Hashing system | Code the hashing system for password protection using 'sha256' to encrypt password and check password in login and registration. | 60 min | March 2 | C
| 15     | Alpha Testing | Test the code for the hashing system. | 5 min | March 2 |  C
| 16     | Create GUI (Graphical User Interface) for login | Use KivyMD (GUI Tool) to create the design and visuals of the login screen. Add text fields to enter information such as email and password. Create buttons to Login and Resgiter. Create labels for welcome tittle. | 120 min | March 4 | C
| 17     | Fix Login GUI (Graphical User Interface) | Fix placing of the text fields, buttons and welcome lable in the Graphical user interface to get a more clean login screen | 60 min | March 5 | C
| 18     | Create GUI (Graphical User Interface) for Register | Use KivyMD (GUI Tool) to create the design and visuals of the register screen. Add text fields to enter information such as email, username, password and check password. Create buttons to go back to login and finalize registration. Create labels for "register" tittle. | 150 min | March 5 | C
| 19     | Create database handler class | Create class named database_handler that provides methods to interact with a SQLite database.This class provides a simple interface for interacting with a SQLite database, including querying the database, inserting or modifying data, and creating tables. | 50 min | March 5 | C
| 20     | Create code for Login system | Code the login system for user to login to Main screen. | 160 min | March 6 | C
| 21     | Create code for registration system | Code the resgistration system for user to be added to the database and be able to log in. | 170 min | March 6 | C
| 22     | Create password policy | Code a password policy that established certain requirements for the user when registering | 50 min | March 6 | C
| 23     | Start Main Screen GUI (Graphical User Interface) | Create the design and visuals of the Main screen. Creat main boxes and tittle labels | 30 min | March 6 | C
| 24     | Create Habit Tracking System pt.1: Labels and checkboxes | Create labels for each habit (5 habits as established on the success criteria), add checkboxes next to the labels and code the activation and deactivation of each checkbox. Connect checkboxes active/disable to database to save information of habit completion | 90 min | March 6 | C
| 25     | Create Habit Tracking System pt.2: Progress Bar | Create Progress bar to display graphically completion of succes criteria. Connect to the habit checkboxes for inmediate update. | 60 min | March 6 | C
| 26     | Create Habit Tracking System pt.3: Progress percentage | Create a label to display percentage accordingly with progress bar and link them together. | 30 min | March 6 | C
| 27     | Create Habit Tracking System pt.4: Date selection | Create a button that displays a calendar to select the day that the habits are being completed. | 20 min | March 6 | C
| 28     | Create Habit Tracking System pt.5: Save button | Create a save button that takes all the information from the checkboxes, progress bar and percentage and date selection and saves it in the database | 30 min | March 6 | C
| 29     | Create History Screen Button | Create a button that takes you to the History Screen | 10 min | March 7 | C
| 30     | Create and code Log out button | Create a log out that takes you to back to the login screen  | 5 min | March 7 | C
| 31     | Fix Main Screen GUI (Graphical User Interface)| Fix the display with all the new additions to the Main Screen to have a more clean and proportional look | 30 min | March 7 | C
| 32     | Create GUI (Graphical User Interface) for History Screen | Use KivyMD (GUI Tool) to create the design and visuals of the history screen. | 30 min | March 7 | C
| 33     | Create code for History of all habits display | Create a table display with all the data obtained form the main screen on the habit completion per day. | 90 min | March 7 | C 
| 34     | Create code for user specific History table display | Create a code that only allows information relevant to the current user to display in the history habit table. | 15 min | March 7 | C
| 35     | Add checkboxes to history table display | Create a code that add checkboxes to display in the history habit table to be able to select the data saved for a specific day. | 20 min | March 7 | C
| 36     | Create delete button | Create a button that allows you to delete the data saved for a specific day that was selected with the checkbox from the history habit table. | 20 min | March 7 | C
| 37     | Create and code back button | Create a button that allows you to go to the Main Screen | 5 min | March 7 | C 
| 38     | Alpha testing | Test the code for the different functionalities created for the habit tracker application. | 15 min | March 8 | C
| 39     | Meeting and Beta testing by client | Meet with the client and let them test the habit tracker. Get feedback on possible improvements/fixes. | 30 min | March 8 | C
| 40     | Fix errors | Modify following the feedback given in the beta testing session with the user | 120 | March 9 | C
| 41     | Alpha testing | Test the code for the different functionalities created for the habit tracker application after the feedback was implemented. | 15 min | March 9 | C
| 42     | Meeting and Beta testing by client | Meet with the client and let them test the habit tracker. Get feedback on possible improvements/fixes. | 30 min | March 9 | C
| 43     | Final approval by client | Obtain approval by the client on the overall development of the habit tracker application | 20 min | March 9 | C
| 44     | Flow diagrams | Draw the flow diagrams for some of the important function inside the code for habit tracker application.  | 90 min | March 9 | C
| 45     | UML Diagram | Draw the UML diagrams for the screen structure and internal functionality for habit tracker application. | 40 min | March 9 | C
## System Diagram

![SYSTEM DIAGRAM P3](https://user-images.githubusercontent.com/111761417/223740333-6ab10612-27bc-4ce5-9bb6-018a3a3c5cb4.jpeg)

<sub>FIG 1. System Diagram is divided in Keyboard and Screen (Connected). Following by the computer (MacBook Air) and Processor (Dual-Core Intel Core i5 1.8GHz 8GB. Next, the Operating System (OS: MacOS 12.5 (21G72). For the software we are using Python 3.10.7. For the GUI (Graphic Unser Interface) we are using KivyMD.uix. Operating inside the software, there is 2 python files (habit_tracker.py and secure_password). Operating inside the GUI, teh is one file (habit_kivy.kv). Lastly, this is connected to the database engine SQLite. There is one database (habit_tracker.db) with 2 tables inside (user and habit).

## Wireframe

![Unit3project-11 2](https://user-images.githubusercontent.com/111761417/224062513-81a3ea07-52fa-49f8-bcc8-3b1e72933740.jpg)
  
<sub>FIG 2. The image displays the Wireframe diagram for the habit tracker. It shows the skeleton of a website or an application's user interface (UI) and core functionality. The Wireframe is divided in Login Screen, Register Screen, Main Screen and History Screen. The application will open in the Login Scrren. Here, the user has the option to login or register. If clicked register, this will take the use to the Register Screen where the user will have the option to go back to the Login Screen or to fill the information required and resgister. If clicked login, the user will be taken to the Main Screen. Here, the user has the option to check boxes to mark habits completed, save the progress, select the date, see history and log out. If clicked log out, the user will be taken back to the Login Screen. If clicked save, the user will save the habits marked by the checkboxes, the day and the percentage of completion. If clicked date, the user will be able to select the date. If clicked history, the user will be take to the History Screen. Here, the user has the option to see history of all habits, delete a day or go back to Main Screen . If clicked Back, the user will be taken back to the Main Screen. If clicked delete, the user will delete the row selected by the checkbox on the history display above.

## Flow Diagrams
  
### CHECKBOX FUNCTIONALITY   
![Unit3project-12](https://user-images.githubusercontent.com/111761417/224130527-81cb9fd7-4fcc-49db-a2b8-6a258de9ce99.jpg)
<sub>FIG 3. The function "checkbox_click updates the state of the checkboxes and the progress bar in response to the user clicking on a checkbox. It also updates a label in the GUI to show the percentage of habits completed. 
  
### SAVING USER'S PROGRESS
  
![Unit3project-13](https://user-images.githubusercontent.com/111761417/224131337-96aec571-69f5-4fca-b2d3-cce50878b298.jpg)
<sub>FIG 4. The function "save" retrieves the progress status of the user's habits, the selected date and user_id, and saves this data into the database after checking if progress for the selected date has already been saved. It also displays an error message if progress is already registered or a confirmation message if the progress is updated successfully.
  
### DELETING SAVED PROGRESS
  
![image](https://user-images.githubusercontent.com/111761417/224131708-a23cbb19-eae1-4d60-83d3-580fff84dd4b.png)

<sub>FIG 5. The function "delete" retrieves the selected rows from the data table of the GUI, loops through each selected row and deletes the corresponding progress data from the database using the unique ID of the row. Once all selected rows have been deleted, the function refreshes the data table in the GUI to display the updated progress data.

## ER Diagram
![er fixed](https://user-images.githubusercontent.com/111761417/224234089-aa2d71d4-f02c-456e-bf23-459ef10e5bc8.jpeg)
<sub>FIG 6. This image shows ER Diagram for the two tables: user, habit.

## UML Diagram
 
![Unit3project-15 (1)](https://user-images.githubusercontent.com/111761417/224138154-991e1f2a-4c8c-4043-812d-87c03d09cc2d.jpg)
<sub>FIG 7. This image shows the UML diagram for the habit tracker. Here are displayed the classes and methods used to develop the application. The diagram includes two main parent classes: MDApp and MDScreen. All subclasses inherit methods and attributes from these parent classes, as indicated by the arrows in the diagram.  

## Test Plan
| Test No | Type of Test                                                |  Date                                                                                               | Procedure | Expected Outcome | |
|---------|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|---------------|------------------------|-----------|
| 1       | Functional: Testing the registration system for the habit tracker application | March 6 | Run habit tracker application > Click on the register button in the Log in screen > Fill the text fields with username, email, password and checked password. > Click on the register button on the register screen > Close the habit tracker application by clicking the log out button > Locate habit_tracker. db database > Find in the main file the user table > Click on user table to open a tab to see the contents of the table > Confirm wether the information inputed in the registration screen has been saved in the user table in the habit_tracker.db database or not | The new user information will be added in the user table in the database habit_tracker.db when following the described procedure.
| 2.      | Functional: Testing the habit tracking system for the habit tracker application  | March 6 | Run habit tracker application > Fill the text fields with email and password in the login screen > Click on the login button in the Log in Screen > Check the habits done for the day with the checkboxes on the main screen > Select the date by clicking on the select date button on the main screen > Save the progress for the day by clicking on the save button on the Main Screen > Close the habit tracker application by clicking the log out button > Locate habit_tracker. db database > Find in the main file the habit table > Click on habit table to open a tab to see the contents of the table > Confirm wether the information selected and saved with the save button on the History Screen has been added in the habit table in the habit_tracker.db database or not. | The progress for the day will added in the user table in the database habit_tracker.db when following the described procedure.
| 3.      | Functional: Testing the delete button on the History Screen to delete saved habit progress | March 6 | Run habit tracker application > Fill the text fields with email and password in the login screen > Click on the login button in the Log in Screen >  Click on the history button on the main screen > Check one checkbox of one of the table rows with the progress saved information for a day > Click the delete button on the History Screen > Close the habit tracker application by clicking the log out button > Locate habit_tracker. db database > Find in the main file the habit table > Click on habit table to open a tab to see the contents of the table > Confirm wether the information selected with the checkbox from the table that displayed the history of the porgress saved on the History Screen has been deleted from the habit table in the habit_tracker.db database or not. | The progress saved information from the table that displayed the history of the porgress saved on the History Screen that was selected with the checkbox will be no longer in the hbait table in the database habit_tracker.db when following the described procedure.  
| 4       | Non-functional: Capabilty for the user to understand the habit tracker application login and registration system independently | March 9 | Run habit tracker application > Give the user only the instruction of registering and then login in to the into the habit tracker without further explanation on how the login and registration system works > see how much does it take the user to figure the registration and login system. | The user will register and login in less than 2 min.
| 5.      | Non-functional: Capabilty for the user to understand the habit tracker application habit tracking system independently | March 9 | Run habit tracker application > Give the user only the instruction of registering the progress of their habits for the day without further explanation on how the habit tracking system works > see how much does it take the user to figure how to save the progress of their habits for the day with the habit tracking system implemented. | The user will register the progress for the day in less than 1 min.
| 6.      | Non-functional: Capabilty for the user to understand how to delete save progress from the history screen | March 9 | Run habit tracker application > Give the user only the instruction of deleting the progress of their habits for the day without further explanation on how the application works > see how much does it take the user to figure how to delete the progress of their habits for the day. | The user will delete the progress for the day in less than 3 min. 

# Criteria C: Development

## Existing Tools
  
* Python
* Pycharm
* ChatGPT
* KivyMD Library
* SQLite Database
* API
* RGB colors

## Techniques applied

* For loops
* If statements
* For loops
* Variables
* Database interaction
* Functions
* Text Formating
* Object Oriented Programming (OOP): Classes, Inheritance

## Computational Thinking 

### CLASS DATABASE HANDLER

```.PY
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
```
The database_hadler class is creating a database handler for SQLite databases. Firslty, the class initializes the database by creating a connection and cursor object in the init method. The parameter is set to namedb that is the name of the database that is going to connect to. Secondly, the search method takes a query as a parameter and executes it using the cursor object. It then returns the results of the query. Following is the run_save method that does the same thing as the searh method (take query as parameter and executes with cursor object) but then commits changes to database using the connection object. Later, the create_tables method creates 2 tables (user and habit) if they do not exist already in the database. Then the run_query will help to execute a query using cursor object and commits the changes to the database with connection object. Lastly,the close method closes the connection to the database. The reasoning behing implementing this class is to provide an organized and consistent way to interact with the SQLite database. It will aid with operations such as querying, saving, creating tables, and closing the connection. This class will make the interaction with the database easier reduces the chances of errors due to inconsistent usage of the database API.makes it easier to write code that interacts with the database and reduces the chances of errors due to inconsistent usage of the database API. Also, the class can be reused across the program, reducing code repetition. 

### LOGIN SYSTEM

```.py
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

```
The Login System from the habit tracker application is inside the Class LoginScreen. This class is a subclass of the MDScreen class and defines the behavior of the login screen of a habit tracker app. Firstly, the try_login method is will be used when the user tries to log in by clicking the "Log In" button on the login screen. Later, the local variables email and pasword are defined. Here is where what the user enters as email and password will be saved. Then, a connection to the database is estalished. A query is created to select the ID and password hash of the user with the given email from the user table of the database and then is executed using search method. Then a password policy is created with if statements. If the query returns a non-empty result, the hashed password is identified using the identify method of the pwd_config module and checked against the password entered by the user using the check_password function. Later, an elif is used to state that if the password entered by the user matches the hashed password in the database, the ID of the user is stored in the user_id variable and the user is redirected to the main screen of the app by changing the current attribute of the parent screen manager to "MainScreen". If the email or password fields are empty or nothing that has been staed before, an error message is displayed and the email and passwd attributes are set to display an error state. The implementation of this login system is effective because allows the user to log into the app securely and verifies information entered by the user.

### TRACKING SYSTEM
  
#### DATE SELECTOR, DISPLAY AND SAVE
```.py

# date selector
def date(self):
    date_dialog = MDDatePicker()
    date_dialog.bind(on_save=self.on_save)
    date_dialog.open()

# saving date selected
def on_save(self, instance, value, data_range):
    self.selected_date = value
    self.ids.progress_date.text = f"{value}"

```
This couple of methods, date and on_save, from the class MainScreen allow the user to clasify the habit progress per day. Here, the date() method creates an instance of MDDatePicker widget and binds the on_save method to its on_save event.Additionally, the on_save method saves the selected date in a class attribute called selected_date and sets the text of a label widget (progress_date) to the selected date. It is good to implement this as it is aked by the client in the succes criteria that there must be a habit progress per day classification. This provide a way for the user to select a date and display it in the user interface.
  
#### CONNECTING CHECKBOXES TO PROGRESS BAR AND DISPLAY PERCENTAGE OF OVERALL HABIT COMPLETION
```.py
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
```
The checkbox_click method from the class MainScreen aids in displaying the percentage of overall completion of habits for the user, connecting the checkboxes to progress bar and percent label. There are 2 arguments in the function: value and habits. Value is the state of the checkbox (True or False), and habits is an integer that specifies which habit the checkbox belongs to. The check state of the checkbox is stored in a list called self.checks, which is initialized to [0, 0, 0, 0, 0] in the init method. If the checkbox is checked (value = True), the corresponding element in the self.checks list is set to 1 and the progress_amount variable is incremented by 20. If checkbox is unchecked (value = False), the corresponding element in the self.checks list is set to 0 and the progress_amount variable is decremented by 20. This will update the progress bar value and label with the new progress_amount. This tracking system provides a simple and intuitive way for users to track their progress towards completing habits and complies with the succes criteria established by the user. Additionally, by using a progress bar and label to display the percentage, users can quickly see how close they are to achieving their goals.

#### SAVE PROGRESS IN DATABASE
  
```.py
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
```
The save method from the class MainScreen aids in saving the user's habit progress into the habit_tracker.db database. Firstly, to make it user specific and only show relevant information to the current logged user, the user ID, progress date, and progress percentage from the MainScreen instance. 
The user's habit progress values from the MainScreen.checks list are also retrieved. The, the program will check if the porgres has been saved for that date. If it has, then it will display an error to the user explaining that the progress has already been saved for the date. If not, the it will insert the progress values and other relevant information into the habit table in the database and will display a message to user to let them know the progress has succesfully been updated. This part of code is very useful as it provides an efficient and reliable way to save the user's habit progress and prevent duplicate entries for the day. Additionally, helpful feedback is given to the user by displaying error messages and success messages, which improves the user experience.

### HISTORY SCREEN
  
#### DISPLAY HISTORY OF ALL HABITS

```.py
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
    self.add_widget(self.data_table)  # add table to the GUI

    # update table
    self.update()
```
The on_pre_enter method from the class History Screen creates a data table in a GUI that displays progress data from the database. Firsltly, it creates an instance of an MDDataTable object with a specific size and position on the screen, as well as a list of column titles and their corresponding widths. Here, the row_pressed method will be used when a row is pressed and the check_pressed method will be called when a checkbox is pressed. Later, adds table to the GUI with add_widget method and then the update method is used to take the data saved in the database and display it on the table for the user to see. The purpose of this code is to fulfill the succes criteria of displaying the history of habit progress per day. Thanks to this, progress is displayed in a clean, understandable and organized manner. 

#### DELETE HABIT PROGRESS FROM HISTORY 

 ```.py
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
 ```
The delete method from the class History Screen is responsible for deleting rows from the database table based on the selection of checkboxes in the MDDataTable widget. The method works by getting the IDs of the rows that were checked, connecting to the SQLite database, constructing a SQL query to delete the corresponding rows, executing the query, and updating the MDDataTable widget after the selected rows have been deleted. This method is useful because allows the user to delete specific rows of data from the habit tracker database. This is important because users may want to remove old or inaccurate data from their progress history, or they may want to clean up their database by removing unused or unnecessary data. By providing this functionality in the app, users can easily manage their progress data and keep their habit tracker organized and up-to-date.
 
#### UPDATE METHOD

```.py
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
  
```
The update method from the class History Screen is responsible for updating the data displayed in an MDDataTable widget. The method retrieves the user ID from the MainScreen instance, constructs a SQL query string to retrieve all rows from the habit table that correspond to the user, connects to the SQLite database, executes the SQL query to retrieve the selected rows, and closes the database connection. Finally, the method calls the update_row_data() method of the MDDataTable widget to update the data displayed. The implementation of this method may be useful because it provides a convenient way to display and update data in a user-friendly format. 
  
# Criteria D: Functionality

### VIDEO IN GOOGLE DRIVE FOLDER
https://drive.google.com/drive/u/0/folders/1lZSkDyv0v5MI3IAEcOer2vDdfn5R5xUJ
  
# Sources
[^1]: “Advantages of Python | Disadvantages of Python.” Python Geeks, 25 June 2021, pythongeeks.org/advantages-disadvantages-of-python/.
[^2]: SQLite. “About SQLite.” Sqlite.org, 2019, www.sqlite.org/about.html.
[^3]: “What Is Database Engine?” Computer Notes, 10 Apr. 2014, ecomputernotes.com/fundamental/what-is-a-database/database engine#:~:text=In%20a%20computer%20database%2C%20the. Accessed 8 Mar. 2023.
[^4]: “What Is a Graphical User Interface (GUI)? - Definition from Techopedia.” Techopedia.com, 2019, www.techopedia.com/definition/5435/graphical-user-interface-gui.
[^5]:



