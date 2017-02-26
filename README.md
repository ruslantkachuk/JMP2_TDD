Test Driven Development
-----------------------
### TASK GENERAL INFORMATION
Should be created application for interaction between mentor and mentee. The main functional interaction between backend and frontend is described as a REST API below.

### REST API:

**1.Mentor**
- 1.1 Get mentor
 - **GET /mentors/{id}** 

- 1.2 Create mentor
 - **POST /mentors** 

   | Name | Type | Description |
   | ---- | ---- | ----------- |
   | firstName | String | First name of mentor |
   | lastName | String | Last name of mentor |
   | email | String | Primary email of user |
   | level | String | There are levels: D1, D2, D3, D4, D5 |
   | mainSkill | String | Main skill, ex: Java, Java Script, C# … |
  ````sh
{
  "firstName": "MentorFirstName",
  "lastName": " MentorLastName ",
  "email": "MentorFirstName_MentorLastName@epam.com",
  "level": "D4",
  "mainSkill": "Java"
}
  ````

- 1.3 Update mentor
 - **PUT /mentors** 

   | Name | Type | Description |
   | ---- | ---- | ----------- |
   | id | int | Identificator of mentor |
   | firstName | String | First name of mentor |
   | lastName | String | Last name of mentor |
   | email | String | Primary email of user |
   | level | String | There are levels: D1, D2, D3, D4, D5 |
   | mainSkill | String | Main skill, ex: Java, Java Script, C# … |
 
- 1.4 Delete mentor
 - **DELETE /mentors/{id}** 

**2.Mentee**
- 2.1 Get mentee
 - **GET /mentees/{id}** 
 
- 2.2 Create mentee
 - **POST /mentees** 
 
- 2.3 Update mentee
 - **PUT /mentees** 
 
- 2.4 Delete mentee
 - **DELETE /mentees/{id}** 

