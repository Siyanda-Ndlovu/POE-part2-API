RaceDay
1. Project Description
RaceDay is an ASP.NET Core Web API developed to support the management of road running, walking and cycling events in South Africa. The system provides functionality for managing events, event categories, participant enrolments and race results.
The API uses a SQL Server database to store information and JWT (JSON Web Token) authentication to help secure endpoints. Role-based authorisation ensures that participants and organisers can access functionality appropriate to their roles.
The project is developed as part of a Software Development assignment, with a focus on RESTful API development, database integration, authentication, authorisation and software testing.
2. Project Objectives
The main objectives of RaceDay are to:

Provide secure user registration and login.
Support participant and organiser roles.
Allow organisers to manage their events and categories.
Support participant enrolments in events.
Allow organisers to record and manage race results.
Store and retrieve information using SQL Server.
Apply authentication and role-based access control to protected endpoints.
Test application functionality using automated unit tests.

User Roles

Participant

Participants can:

Register and log in.

Access authorised participant functionality.

View events and categories through the relevant API endpoints.

Access their enrolment and result information where supported by the API.

Organiser

Organisers can:

Register and log in.

Create and manage events they organise.

Manage event categories where authorised.

View relevant enrolment information where supported.

Record and manage results for eligible enrolments.

Access to protected endpoints is controlled using JWT authentication and role-based authorisation.

4. Technologies Used

Programming language: C#

Framework: ASP.NET Core Web API

Target framework: .NET 8

Database: Microsoft SQL Server

Data access: Entity Framework Core

API documentation and testing: Swagger / OpenAPI

Authentication: JWT (JSON Web Tokens)

Password security: ASP.NET Core PasswordHasher

Unit testing: xUnit

Development environment: Microsoft Visual Studio

5. Main API Features

Authentication

User registration

User login

Password hashing

JWT token generation

Role-based authorisation

Event Management

Retrieve event information

Create events where authorised

Update and delete events where supported and authorised

Category Management

Retrieve event categories

Create categories where authorised

Update and delete categories where supported and authorised

Enrolments

Manage participant enrolments through the available enrolment endpoints.

Results

Retrieve authorised result information

Create results for eligible enrolments

Update or delete results where authorised

The available routes, request formats and responses can be inspected through Swagger when the API is running.

6. Database

The project uses a SQL Server database named RaceDay.

The database contains the following main tables:

Users – stores user account information and roles.

Organiser – stores organiser records linked to users.

Participant – stores participant records linked to users and events in the current design.

Event – stores event information.

Category – stores event category information.

Enrolment – stores participant enrolments.

Result – stores race results associated with enrolments.

Entity Framework Core is used to connect the API to SQL Server and perform database operations.

7. Getting Started

Prerequisites

Before running the project, ensure that you have:

Microsoft Visual Studio with the ASP.NET and web development workload.

.NET 8 SDK.

Microsoft SQL Server.

SQL Server Management Studio (SSMS), or an equivalent SQL management tool.

Step 1: Clone or download the project

Obtain the project source code and open the solution file (.sln) in Visual Studio.

Step 2: Configure the database connection

Open appsettings.json and check the connection string under ConnectionStrings.

Update the server and database details to match your local SQL Server installation.

Example:

{

  "ConnectionStrings": {
    "DefaultConnection": "Server=PEARL\\MSSQSERVER1;Database=RaceDay;Trusted_Connection=True;TrustServerCertificate=True;"
  },

