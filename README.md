College Event Management System (CEMS)
Project Overview:

The College Event Management System (CEMS) is a comprehensive web application that simplifies the process of managing events on a college campus. The system allows administrators to create, update, and manage events while enabling students to view, register, and participate in these events. CEMS ensures efficient coordination between event coordinators, participants, and organizers by providing a streamlined user experience and a well-structured database schema.

Table of Contents
Project Overview
Features
Technologies Used
Installation and Setup
Database Schema
Usage
Contributors
License
Features
Event Creation and Management:

Admins can create, edit, or delete events.
Events include details such as title, description, date, time, location, and event capacity.
Event Registration:

Students can browse and register for upcoming events.
Real-time updates on available seats based on event capacity.
Coordinator Management:

Event coordinators can manage participant details.
User Roles:

Roles include Administrator, Coordinator, and Participant, each with unique access and functionality.
Notifications:

Email/SMS notifications for successful registration and event reminders (optional feature).
Technologies Used
Frontend:

HTML5, CSS3
JavaScript, jQuery (for interactive UI components)
Backend:

PHP (for server-side logic)
Database:

MySQL (for storing event, participant, and coordinator data)
Additional Tools:

Bootstrap (for responsive design)
phpMyAdmin (for database management)
Installation and Setup
Prerequisites
A local server (e.g., XAMPP, WAMP)
PHP 7.x or later
MySQL 5.7 or later
Web browser (for testing and using the application)
Steps
Clone the Repository:

bash
Copy code
git clone https://github.com/yourusername/CEMS.git
Start Local Server:

Start Apache and MySQL from XAMPP/WAMP.
Configure Database:

Import the cems.sql file in your MySQL database. This file contains the database schema and initial seed data.
Update database connection settings in the config.php file (include host, username, password, and database name).
Run the Application:

Open your web browser and navigate to http://localhost/CEMS.
You should see the homepage where users can view upcoming events.
File Structure
arduino
Copy code
CEMS/
│
├── css/
│   └── styles.css
├── js/
│   └── main.js
├── images/
│   └── (Event-related images)
├── aboutus.php
├── adminPage.php
├── createEventForm.php
├── register.php
├── viewEvent.php
├── config.php
└── cems.sql
Database Schema
Tables:
Events - Stores details about each event.

event_id, event_name, event_description, event_date, event_time, event_capacity, coordinator_id, etc.
Participants - Stores participant details.

participant_id, name, email, phone_number, event_id (foreign key to Events).
Coordinators - Manages event coordinators.

coordinator_id, name, email, phone_number.
Event Info - Links participants to events.

info_id, event_id (foreign key to Events), participant_id (foreign key to Participants).
Usage
Admin:

Login to the admin panel using credentials.
Create new events by filling out the event creation form.
Edit or delete existing events.
Students:

View a list of upcoming events on the homepage.
Register for events by filling out the registration form.
Receive a confirmation email upon successful registration.
Coordinator:

View participant details for events they are managing.
Contributors
[Your Name] – Developer and Project Architect
Additional Contributors: List any collaborators here.
