Race_Day
1. Project Overview

Race_Day is a race management system designed to manage runners, race events, registrations, categories, payments, results, locations, organisers, and sponsors.

The system provides a structured SQL Server database and a planned REST API for managing race-day information.

2. Project Objectives

The main objectives of the Race_Day system are to:

Allow users/runners to register and log in.
Allow runners to manage their profiles.
Display available race events.
Manage race categories.
Allow authenticated runners to enrol in events.
Allow organisers and administrators to manage events and categories.
Record and manage race results.
Manage registrations and payments.
Store race locations, organisers, and sponsors.

3. Planning Documents

All planning documents are stored in the /docs folder and must be completed before application/API implementation.

ERD

The Entity Relationship Diagram defines the database entities, attributes, primary keys, foreign keys, relationships, and cardinalities.

File:

/docs/Race_Day_ERD.pdf



API Endpoint Plan

The API Endpoint Plan defines the REST API routes, HTTP methods, descriptions, required roles, request bodies, and expected responses.

File:


SQL Database Script

The SQL script creates the complete SQL Server database, tables, constraints, relationships, and sample data.

File:

/docs/Race_Day.sql


4. Database

The project uses Microsoft SQL Server.

Database name: Race_Day

The database contains the following entities:

RUNNER
REGISTRATION
RACE
LOCATION
ORGANIZER
PAYMENT
RACE_RESULT
RACE_CATEGORY
SPONSOR
RACE_SPONSOR

The database includes primary keys, foreign keys, unique constraints, default values, and validation checks.

5. API Structure

The API is organised into the following functional areas:

Authentication
User Profiles
Events
Categories
Event Enrolments
Results

Example routes include:

POST /api/auth/register
POST /api/auth/login
GET /api/users/me
GET /api/events
GET /api/events/{eventId}/categories
POST /api/events/{eventId}/enrolments
GET /api/events/{eventId}/results

The implemented API should closely follow the endpoint plan in /docs/Race_Day_API_Endpoint_Plan.docx.

6. User Roles
Public

Users who are not logged in. They can access publicly available event and result information and create an account.

Authenticated User

A logged-in runner who can manage their profile and enrol in races.

Organizer

An organiser can manage events and categories and manage race enrolments and results as permitted by the API.

Administrator

An administrator has management access to events, categories, enrolments, and results.

7. Sample Data

The SQL script contains realistic sample data, including:

2 organisers
3 runners
3 race events
Categories for each event
Sample enrolments
Sample payments
Sample race results
Sponsors and race-sponsor relationships
Race locations
8. Technologies

The planned system uses:

C#
ASP.NET Core Web API
Microsoft SQL Server
SQL Server Management Studio (SSMS)
REST API
Git and GitHub
9. Repository Structure
Race_Day/
│
├── docs/
│   ├── Race_Day_ERD.pdf
│   ├── Race_Day_API_Endpoint_Plan.docx
│   └── Race_Day.sql
│
├── README.md
│
└── [API/application source code]
10. Development Approach

The system is planned before implementation. The development process follows these stages:

Analyse the system requirements.
Design the database ERD.
Plan all API endpoints.
Create the SQL Server database script.






