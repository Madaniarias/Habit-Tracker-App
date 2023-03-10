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
![Unit3project-16](https://user-images.githubusercontent.com/111761417/224141791-d91c9d79-258f-4eed-9965-3b3040f71e40.jpg)
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
* if statements
* For loops
* Variables
* Database interaction
* Functions
* Text Formating
* Object Oriented Programming (OOP): Classes, Inheritance

## Computational Thinking 

# Criteria D: Functionality

## Sources

[^1]: “Advantages of Python | Disadvantages of Python.” Python Geeks, 25 June 2021, pythongeeks.org/advantages-disadvantages-of-python/.
[^2]: SQLite. “About SQLite.” Sqlite.org, 2019, www.sqlite.org/about.html.
[^3]: “What Is Database Engine?” Computer Notes, 10 Apr. 2014, ecomputernotes.com/fundamental/what-is-a-database/database engine#:~:text=In%20a%20computer%20database%2C%20the. Accessed 8 Mar. 2023.
[^4]: “What Is a Graphical User Interface (GUI)? - Definition from Techopedia.” Techopedia.com, 2019, www.techopedia.com/definition/5435/graphical-user-interface-gui.
[^5]:



