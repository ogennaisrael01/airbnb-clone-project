# Airbnd clone project

# Project Overview
Project Description
This project is a backend clone of Airbnb, designed to simulate the core functionalities of a property rental platform. It includes user authentication, property listings, bookings, and reviews. 

# Team stack 
* Backend: Django / Django REST Framework

* Database: PostgreSQL / SQLite

* Django REST Framework (DRF)

* Authentication: JWT (SimpleJWT or djangorestframework-simplejwt)

* Deployment: Docker + Uvicorn 

* Celery: For background task processing

* Redis: For caching and real-time updates

* Testing: Pytest, Postman

* Version Control: Git + GitHub

* Documentation: Swagger / Postman

* API Versioning: Implement versioning for the API endpoints

* CI/CD: GitHub Actions


# Team Roles
1. Project Manager / Team Lead
* Coordinates team meetings and progress tracking

* Ensures milestones and deliverables are met

* Reviews pull requests and enforces coding standards

2. Backend Developer (Core APIs)
* Responsible for implementing API endpoints, database schemas and business logic.
* Implements serializers, views, and model logic (Django/DRF)
* Writes unit and integration tests for APIs

3. DevOps / Deployment Lead
* Sets up Docker and environment configs

* Manages deployment to cloud platforms (Heroku, Render, etc.)

* Ensures logging, backups, and performance monitoring

4. QA & Testing Engineer
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
1. User
> Represents: Guests and Hosts

<Relationships:

* One-to-many with Listings (a host can create many listings)

* One-to-many with Bookings (a user can book many listings)

* One-to-many with Reviews (a user can write many reviews)

2. Listing
> Represents: Properties available for rent

<Relationshships 

* Many-to-one → User (a user can have many listings)

* One-to-many with Bookings(one listing can have many bookings)

* One-to-many with Reviews(one listing can have many reviews )

3. Booking
> Represents: A user booking a listing
<Relationships:

* Many-to-one → User(a user can have many bookings)

* Many-to-one → Listing(can have many bookings in one listings)

4. Review
> Represents: Feedback left by a guest
<Relationships

* Many-to-one → User(a user can have many reviews)

* Many-to-one → Listing(a listing can have many reviews)

5. Payment
> Represents: A user payment for a booking
<Relationships 

* Each Booking has one corresponding Payment

* One User can have many Payments

# API Security
Security Measures & Their Importance
1. JWT authentications: Use JWT tokens for stateless authentication.
* Why: Secures API access; token expiry limits exposure if stolen. Refresh tokens allow controlled renewal.

2.  Rate Limiting:  Limit API request rate per user or IP
* why: Blocks brute-force attacks, abuse, and API spamming.

3. Database Security: 
* why: Protects against direct DB access and accidental exposure of sensitive data.

4. Logging and Monitoring:
* Why: Detect suspicious behavior, errors, and potential breaches.
5.  Password Hashing
* Why: Prevents plain-text password storage and protects user credentials even if the DB is breached.

# Feature Breakdown
1. User Authentication & Authorization
Sign up, login, logout, and role-based access (guest or host).

2. Property Listings Management
Hosts can create, update, and delete property listings with descriptions, photos, and pricing.

3.  Booking System
Guests can check availability, select dates, and book listings

4. Payment Integration
Users can pay for bookings using a payment gateway

# CI/CD Pipeline
What Is CI/CD?
> CI/CD is the process of automatically testing, integrating, and deploying code changes to ensure faster, safer, and more reliable software delivery.


Why CI/CD Is Important for Your Airbnb Clone Project
1. faster development
2. fewer bugs in production
3. Team collaboration
4. scalability

CI/CD Tools
1. GitHub Actions
2. CircleCI
3. GitLab CI/CD
4. Jenkins


project setup
1. Clone the repository:
```bash
git clone <https://github.com/ogennaisrael01/airbnb-clone-project>
cd airbnb-clone-project
```

2. Create and activate a virtual environment (optional but recommended):
```bash
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
```
3. Install dependencies:
```bash
pip install -r requirements.txt
```
4. Set up environment variables:
Create a .env file in the project root and add necessary environment variables (e.g., SECRET_KEY, DATABASE_URL).

5. Apply database migrations:
```bash
python manage.py migrate
