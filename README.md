# Airbnd clone project

# 🏡 Airbnb Clone – Project Overview
📌 Project Description
This project is a backend clone of Airbnb, designed to simulate the core functionalities of a property rental platform. It includes user authentication, property listings, bookings, and reviews. 

# Team stack 
* Backend: Django / Django REST Framework

* Database: PostgreSQL / SQLite

* Django REST Framework (DRF)

* Authentication: JWT (SimpleJWT or djangorestframework-simplejwt)

* Deployment: Docker + Gunicorn + Nginx (optional)


# Team Roles
🧠 1. Project Manager / Team Lead
* Coordinates team meetings and progress tracking

* Ensures milestones and deliverables are met

* Reviews pull requests and enforces coding standards

🏗️ 2. Backend Developer (Core APIs)
* Responsible for implementing API endpoints, database schemas and business logic.
* Implements serializers, views, and model logic (Django/DRF)
* Writes unit and integration tests for APIs

📦 3. DevOps / Deployment Lead
* Sets up Docker and environment configs

* Manages deployment to cloud platforms (Heroku, Render, etc.)

* Ensures logging, backups, and performance monitoring

✅ 4. QA & Testing Engineer
* Writes and runs unit, integration, and API tests

* Uses Postman or Swagger for endpoint testing

* Identifies bugs and creates test cases

* Assists with CI/CD setup if applicable

# Technology Stack
* Django / Django REST Framework: The core backend framework used to build the web application logic.

* PostgreSQL / SQLite:  Builds RESTful APIs that allow frontend or mobile apps to interact with the backend.

Authentication: JWT (SimpleJWT or djangorestframework-simplejwt):  Securely handles user authentication without storing sessions on the server.

*  Django REST Framework (DRF):  Builds RESTful APIs that allow frontend or mobile apps to interact with the backend.

* Docker: Packages the app with all its dependencies to run reliably on any system.

# Database Design
🔹 1. User
> Represents: Guests and Hosts

<Relationships:
* One-to-many with Listings (a host can create many listings)

* One-to-many with Bookings (a user can book many listings)

* One-to-many with Reviews (a user can write many reviews)