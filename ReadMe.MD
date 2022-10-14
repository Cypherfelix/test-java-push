First Step is to Create a database in this assignment my database
is called assignment


The sql query to be executes is

    CREATE DATABASE assignment
        WITH
        OWNER = postgres
        ENCODING = 'UTF8'
        TABLESPACE = pg_default
        CONNECTION LIMIT = -1
        IS_TEMPLATE = False;


The request to be made are as follows

Register new Employee:

   ----app.post("/employee/register", employee.register);
METHOD: POST
URL: http://localhost:8080/employee/register
Body: JSON
    {
        "firstname": "Felix",
        "lastname": "marvin",
        "email": "fulldevtutor@gmail.com",
        "password": "12345"
    }


Log In Employee
   ---- app.get("/employee/login", employee.login);
METHOD: GET
URL: http://localhost:8080/employee/login
Body: json
   {
       "email": "fulldevtutor@gmail.com",
       "password" : "12345"
   }

Employee Create Ticket:
    ----app.post("/employee/create-tickets", employee.addTicket);
METHOD: GET
URL: http://localhost:8080/employee/create-tickets
Body: json
    {
        "user_id" : 1,
        "description" : ""
    }


Employee Get Tickets
    -----app.get("/employee/view-tickets/{id}", employee.viewMyTickets);
Add an id at the url end
METHOD: GET
URL: http://localhost:8080/employee/view-tickets/1



Manager:

Manager Login
-----app.get("/manager/login", managerController.login);
METHOD: GET
URL: http://localhost:8080/manager/login
Body: json
    {
    "email": "fulldevtutor2@gmail.com",
    "password" : "12345"
    }

Manager register
----app.post("/manager/register", managerController.register);
METHOD: POST
URL: http://localhost:8080/employee/register
Body: JSON
    {
    "firstname": "Felix",
    "lastname": "marvin",
    "email": "fulldevtutor2@gmail.com",
    "password": "12345"
    }

Manager View Tickets
METHOD:GET
URL: http://localhost:8080/manager/view-tickets

Manager Approve Ticket
------app.put("/manager/approve/{id}", managerController.approve);
METHOD: PUT
URL: http://localhost:8080/employee/approve/{id}
replace {id} with a ticket id


Manager Deny Ticket
------app.put("/manager/deny/{id}", managerController.approve);
METHOD: PUT
URL: http://localhost:8080/employee/deny/{id}
replace {id} with a ticket id


Manager View Pending
METHOD:GET
URL: http://localhost:8080/employee/view-pending

Manager View approved
METHOD:GET
URL: http://localhost:8080/employee/view-approved

Manager View denied
METHOD:GET
URL: http://localhost:8080/employee/view-denied
