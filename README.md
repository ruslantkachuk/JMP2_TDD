Test Driven Development
-----------------------
[![Build Status](https://travis-ci.org/ruslantkachuk/JMP2_TDD.svg?branch=master)](https://travis-ci.org/ruslantkachuk/JMP2_TDD)

### TECHNOLOGY STACK
Spring Boot (web, test, jpa), HSQLDB, MariaDB, Mockito, DbUnit, Gradle

**Build project**: gradle build

**Run tests**: gradle test

**Run project**: gradle bootRun

### TASK GENERAL INFORMATION
Should be created application for interaction between mentor and mentee. The main functional interaction between backend and frontend is described as a REST API below.

### REST API:

**1.Mentor**
- 1.1 Get mentor
 - **GET /mentors/{id}** 

- 1.2 Get list of mentor's mentees
 - **GET /mentors/{id}/mentees** 
 
- 1.3 Get list of mentors by skill
 - **GET /mentors?skill={skill}**
 
- 1.4 Create mentor
 - **POST /mentors** 

   | Name | Type | Description |
   | ---- | ---- | ----------- |
   | firstName | String | First name of mentor |
   | lastName | String | Last name of mentor |
   | email | String | Primary email of mentor |
   | level | String | There are levels: D1, D2, D3, D4, D5 |
   | mainSkill | String | Main skill, ex: Java, Java Script, C# … |
     
     ```sh
     {
         "firstName": "MentorFirstName",
         "lastName": " MentorLastName ",
         "email": "MentorFirstName_MentorLastName@epam.com",
         "level": "D4",
         "mainSkill": "Java"
     }
     ```

- 1.5 Update mentor
 - **PUT /mentors** 

   | Name | Type | Description |
   | ---- | ---- | ----------- |
   | id | int | Identificator of mentor |
   | firstName | String | First name of mentor |
   | lastName | String | Last name of mentor |
   | email | String | Primary email of mentor |
   | level | String | There are levels: D1, D2, D3, D4, D5 |
   | mainSkill | String | Main skill, ex: Java, Java Script, C# … |
     
     ```sh
     {
         "id": 100,
         "firstName": "MentorFirstName",
         "lastName": " MentorLastName ",
         "email": "MentorFirstName_MentorLastName@epam.com",
         "level": "D4",
         "mainSkill": "Java"
     }
     ```
 
- 1.6 Delete mentor
 - **DELETE /mentors/{id}** 

**2.Mentee**
- 2.1 Get mentee
 - **GET /mentees/{id}** 
 
- 2.2 Create mentee
 - **POST /mentees** 
 
   | Name | Type | Description |
   | ---- | ---- | ----------- |
   | firstName | String | First name of mentee |
   | lastName | String | Last name of mentee |
   | email | String | Primary email of mentee |
   | level | String | There are levels: D1, D2, D3, D4, D5 |
   | mainSkill | String | Main skill, ex: Java, Java Script, C# … |
   | idMentor | int | Identificator of mentor |
     
     ```sh
     {
         "firstName": "MenteeFirstName",
         "lastName": " MenteeLastName ",
         "email": "MenteeFirstName_MenteeLastName@epam.com",
         "level": "D3",
         "mainSkill": "Java",
         "idMentor": 100
     }
     ```

- 2.3 Update mentee
 - **PUT /mentees** 
 
   | Name | Type | Description |
   | ---- | ---- | ----------- |
   | id | int | Identificator of mentee |
   | firstName | String | First name of mentee |
   | lastName | String | Last name of mentee |
   | email | String | Primary email of mentee |
   | level | String | There are levels: D1, D2, D3, D4, D5 |
   | mainSkill | String | Main skill, ex: Java, Java Script, C# … |
   | idMentor | int | Identificator of mentor |
     
     ```sh
     {
         "id": 200,
         "firstName": "MenteeFirstName",
         "lastName": " MenteeLastName ",
         "email": "MenteeFirstName_MenteeLastName@epam.com",
         "level": "D3",
         "mainSkill": "Java",
         "idMentor": 100
     }
     ```
 
- 2.4 Delete mentee
 - **DELETE /mentees/{id}** 

