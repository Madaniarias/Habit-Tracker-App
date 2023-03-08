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
Regarding the process to achieve the proposed solution, an overview of the steps is: 
1) Requirement gathering: meeting with client the get a better understanding of the client's problem and needs. Establish success criteria.
2) Design, Wireframes and Diagrams: Create visual representations of the proposed solution, contributing to a more hollistic understanding of the techniques and methods used.
3) Development: start development of proposed solution following the criteria established by the client.
4) Prototype Demo: Show the demo application to the client and get feedback
5) Changes and Confirmation: Take feedback and make changes accordingly.

## Design statement

I will design and make a habit tracker application for a highschool student. The project will be about designing that helps her visualize, organize and keep track of her progress in the course of developing good habits and will be constructed using the software Python 3.10.7, SQLite (database engine) and KivyMD (Graphical User Interface tool). It will take about 4 weeks to make and will be evaluated according to the criteria below.

## Success Criteria

1. The solution provides a login screen that uses email and is protected by password. Also, povides a registration screen that requests username, email, password and checks the password.
2. The solution will display the history of all habits. It will show the completion of each individual habit and overall habit completion of a particular day.
3. The solution provides a tracking system for up 5 habits.
4. The solution allows the user to save habit completion per day and displays the progress in a graphic manner.
5. The solution's overall application displays should mostly use the color palette provided by the client and buttons should be a distingable size.
6. The solution should include a log out button for the user to close the session.

Color palette provided:

Habits agreed on:

# Criteria B: Design

## Record of Tasks
| Task No | Planned Action                                                | Planned Outcome                                                                                                 | Time estimate | Target completion date | Criterion |
|---------|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|---------------|------------------------|-----------|
| 1      | Planning: First meeting with client |  Getting a sense of what is the problem and the needs of the client. Start to get a deeper understanding of how does the desire interface looks for the client. Note taking on the meeting  | 6min                  | Feb 9 | A
| 2      | Analysis of planning meeting | Taking information learnt form the first meeting with the client to see what was understood from the developer part and present next meeting with client to confirm if the information was understood correctly. |  10 min  | Feb 9 | A
| 3      | Planning: Second meeting with client | Getting a sense of what is the problem and the needs ofthe client. Go together through the information again and understand can be made and what cannot. Note taking on the meeting | 5 min | Feb 21 | A
| 4      | Analysis of planning meeting | Taking information learnt form the second meeting with the client to see what was understood from the developer part and present next meeting with client to confirm if the information was understood correctly. | 15 min | Feb 21 | A
| 5      | Problem definition | After the meetings with the client, establish the problem that the project is going to be solving specifically and what are the main needs of the client | 20 min | Feb 23 | A
| 6      | Rationale for Proposed Solution |  | 10 min | Feb 23 | A
| 7      | Design statement |  | 5 min | Feb 23 | A
| 8      | Succes criteria |  | 5 min | Feb 23 |  A
| 9      | Approval of Criteria A by the client|  | 20 min | Feb 23 | A 
| 10     | System Diagram |  |  | Feb 23 |  B
| 11     | Wireframe |  |  |  | 
| 12     | Flow Diagrams |  |  |  | 
| 13     | ER Diagrams |  |  |  | 
| 14     |  |  |  |  | 
| 15     |  |  |  |  |  
| 16     |  |  |  |  | 
| 17     |  |  |  |  | 
| 18     |  |  |  |  | 
| 19     |  |  |  |  |
| 20     |  |  |  |  |

## System Diagram

## Wireframe

## Flow Diagrams

## ER Diagrams

## UML Diagrams

## Test Plan
| Test No | Type of Test                                                |  Date                                                                                               | Procedure | Expected Outcome | |
|---------|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|---------------|------------------------|-----------|
| 1       | Functional:  |  |  |  
| 2.      | Functional:  |  |  |  
| 3.      | Functional:  |  |  |  
| 4       | Non-functional:  |  |  |  
| 5.      | Non-functional:  |  |  |  
| 6.      | Non-functional:  |  |  |  

# Criteria C: Development

## Existing Tools

## Techniques applied

## Computational Thinking 

# Criteria D: Functionality

## Sources

[^1]: “Advantages of Python | Disadvantages of Python.” Python Geeks, 25 June 2021, pythongeeks.org/advantages-disadvantages-of-python/.
[^2]: SQLite. “About SQLite.” Sqlite.org, 2019, www.sqlite.org/about.html.
[^3]: “What Is Database Engine?” Computer Notes, 10 Apr. 2014, ecomputernotes.com/fundamental/what-is-a-database/database engine#:~:text=In%20a%20computer%20database%2C%20the. Accessed 8 Mar. 2023.
[^4]: “What Is a Graphical User Interface (GUI)? - Definition from Techopedia.” Techopedia.com, 2019, www.techopedia.com/definition/5435/graphical-user-interface-gui.
[^5]:



