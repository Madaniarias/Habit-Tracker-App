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

A highschool student, Lison Hebert, is interested in building good habits to improve her daily rutine and help her reach your goals. She has been manually keeping track of her habit completion in a personal diary, however at the moment this method has become too time consuming and tedious to keep track off. It is also difficult for the highschool student to see the progresss in an organized manner. The client is in need of a habit tracker application that helps her visualize, organize and keep track of her progress in the course of developing good habits. 

## Rationale for Proposed Solution

Considering the client requirements an adequate solution includes a habit tracker application that helps her visualize, organize and keep track of her progress in the course of developing good habits. For a this application it may adequate to consider a computer program with a GUI( Graphical User Interface) that can store data into a database. 

For a low cost sensing device an adequate alternative is the DHT11 sensor1 which is offered online for less than 5 USD and provides adequare precision and range for the client requirements (Temperature Range: 0°C to 50°C, Humidity Range: 20% to 90%). Similar devices such as the DHT22, AHT20 or the AM2301B 2 have higher specifications, however the DHT11 uses a simple serial communication (SPI) rather than more eleborated protocols such as the I2C used by the alternatives. For the range, precision and accuracy required in this applicaiton the DHT11 provides the best compromise. Connecting the DHT11 sensor to a computer requires a device that provides a Serial Port communication. A cheap and often used alternative for prototyping is the Arduino UNO microcontroller 3. "Arduino is an open-source electronics platform based on easy-to-use hardware and software"4. In additon to the low cost of the Arduino (< 6USD), this devide is programable and expandable1. Other alternatives include diffeerent versions of the original Arduino but their size and price make them a less adequate solution.

Considering the budgetary constrains of the client and the hardware requirements, the software tool that I proposed for this solution is Python. Python is open source, it is mature and supported in mutiple platforms (platform-independent) including macOS, Windows, Linux and can also be used to program the Arduino microprocessor 56. In comparison to the alternative C or C++, which share similar features, Python is a High level programming language (HLL) with high abstraction 7. For example, memory management is automatic in Python whereas it is responsability of the C/C++ developer to allocate and free up memory 7, this could result in faster applications but also memory problems. In addition a HLL language will allow me and future developers extend the solution or solve issues proptly.

## Design statement

## Success Criteria

1. The solution provides a login screen utilizing email and will be protected by password and a registration screen rquesting username, email, password and check the password to create a new user.
2. The solution will display all habit history, showing per day the completion per each individual habit and overall habit completion of the particular day. 
3. The solution provides a tracking system for up 5 habits.
4. The solution allows the user to save habit completion per day and displays the progress graphically.
5. The solution's overall application displays should mostly use color provided in the color pallette and buttons should be a distingable size.
6. The solution should include a log out button for the user to close the session.

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
