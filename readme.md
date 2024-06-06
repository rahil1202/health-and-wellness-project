# Health and Wellness Practitioners Platform

## Project Overview

This project aims to create a comprehensive platform for health and wellness practitioners to manage their practices, interact with patients, and analyze key data related to their marketing efforts. The platform includes features for appointment booking, practice analytics, website management, and patient check-in.

## Technology Stack

### Frontend
- **Framework:** React.js
- **Styling:** Tailwind CSS and Material UI
- **State Management:** Redux 
- **Routing:** React Router
- **HTTP Client:** Axios

### Backend
- **Language:** Java
- **Framework:** Spring Boot
- **Database:** SQL
- **ORM:** Hibernate

### Database
- **Type:** Relational Database
- **Database Management System:** MySQL



## Project Design

```
+---------------------+              +----------------------+              +----------------------+
|      Frontend       |              |       Backend        |              |      Database        |
|  (React Components) |              |  (Spring Controllers)|              |     (MySQL Tables)   |
|                     |              |                      |              |                      |
|  +---------------+  |   HTTP API   |  +----------------+  |  JPA Queries |  +----------------+  |
|  | Login.js       |<------------->|  | AuthController  |<------------->|  | Practitioners   |  |
|  +---------------+  |              |  +----------------+  |              |  +----------------+  |
|  +---------------+  |              |  +----------------+  |              |  +----------------+  |
|  | Signup.js      |<------------->|  | ApptController  |<------------->|  | Appointments    |  |
|  +---------------+  |              |  +----------------+  |              |  +----------------+  |
|  +---------------+  |              |  +----------------+  |              |  +----------------+  |
|  | Dashboard.js   |<------------->|  | AnalyticsCtrl   |<------------->|  | Analytics       |  |
|  +---------------+  |              |  +----------------+  |              |  +----------------+  |
|  ...               |              |  ...                |              |  ...                |
+---------------------+              +----------------------+              +----------------------+
```

## Project Structure

### Frontend

```
frontend/
├── public/
│   ├── index.html
│   ├── favicon.ico
│   └── manifest.json
├── src/
│   ├── components/
│   │   ├── Authentication/
│   │   │   ├── Login.js
│   │   │   ├── Signup.js
│   │   │   ├── ForgotPassword.js
│   │   ├── Dashboard/
│   │   │   ├── Home.js
│   │   │   ├── Appointments.js
│   │   │   ├── Analytics.js
│   │   │   ├── WebsiteAnalytics.js
│   │   │   ├── SEOStats.js
│   │   │   ├── Messages.js
│   │   │   ├── Reviews.js
│   │   │   ├── WebsiteEditor.js
│   │   │   ├── BlogManager.js
│   │   │   ├── SocialMedia.js
│   │   │   ├── Profile.js
│   │   ├── CheckIn/
│   │   │   ├── CheckIn.js
│   │   │   ├── Confirmation.js
│   ├── pages/
│   │   ├── Dashboard.js
│   │   ├── Login.js
│   │   ├── Signup.js
│   │   ├── ForgotPassword.js
│   │   ├── CheckIn.js
│   ├── App.js
│   ├── index.js
│   ├── api/
│   │   ├── api.js
│   ├── styles/
│   │   ├── styles.css
│   ├── utils/
│       ├── helpers.js
```

### Backend

```
backend/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   ├── com/
│   │   │   │   ├── healthwellness/
│   │   │   │   │   ├── controller/
│   │   │   │   │   │   ├── AuthController.java
│   │   │   │   │   │   ├── AppointmentController.java
│   │   │   │   │   │   ├── AnalyticsController.java
│   │   │   │   │   ├── model/
│   │   │   │   │   │   ├── Practitioner.java
│   │   │   │   │   │   ├── Patient.java
│   │   │   │   │   ├── repository/
│   │   │   │   │   │   ├── PractitionerRepository.java
│   │   │   │   │   │   ├── PatientRepository.java
│   │   │   │   │   ├── service/
│   │   │   │   │   │   ├── PractitionerService.java
│   │   │   │   │   │   ├── PatientService.java
│   │   │   │   │   ├── utils/
│   │   │   │   │   │   ├── JwtUtil.java
│   │   ├── resources/
│   │   │   ├── application.properties
│   │   │   ├── schema.sql
│   │   │   ├── data.sql
│   ├── test/
│       ├── java/
│           ├── com/
│               ├── healthwellness/
│                   ├── controller/
│                       ├── AuthControllerTest.java
│                       ├── AppointmentControllerTest.java
```

## Component Diagram

```
+-----------------------------------------------------------+
|                       Cloud Infrastructure                |
|  +----------------+     +----------------+                |
|  |   Load Balancer|     |   CDN          |                |
|  +-------+--------+     +-------+--------+                |
|          |                      |                         |
|          |                      |                         |
|  +-------v--------+    +--------v------+                  |
|  |   Frontend     |    |   Backend      |                  |
|  |  (React.js)    |    | (Spring Boot)  |                  |
|  +-------+--------+    +--------+-------+                  |
|          |                      |                         |
|          |                      |                         |
|  +-------v--------+    +--------v-------+   +------------+ |
|  |   External     |    |   Database     |   | Third-Party| |
|  |   Services     |    | (PostgreSQL)   |   | Services   | |
|  | (Google, Yelp, |    +--------+-------+   | (Twilio,   | |
|  | Dialogflow,    |             |           | SendGrid)  | |
|  | Analytics, SEO)|             |           +------------+ |
|  +----------------+             |                         |
|                                 |                         |
|                      +----------v--------+                |
|                      |  Data Warehouse   |                |
|                      |  (for Analytics)  |                |
|                      +-------------------+                |
+-----------------------------------------------------------+
```

## High-Level System Design

### Architecture

The platform follows a typical client-server architecture with the following components:

1. **Frontend (Client):** A React.js application that provides an interactive user interface for practitioners and patients. The frontend communicates with the backend via RESTful APIs.

2. **Backend (Server):** A Java Spring Boot application that handles business logic, processes requests from the frontend, and interacts with the database.

3. **Database:** A MySQL relational database that stores all persistent data related to practitioners, patients, appointments, analytics, and more.

### Key Components

- **Authentication:**
  - User signup, login, and password management
  - JWT-based authentication

- **Practitioner Dashboard:**
  - Home/Dashboard: Overview of key metrics
  - Appointments Calendar: Manage appointments
  - Practice Analytics: View monthly patient acquisition and revenue stats
  - Website Analytics: Track website visitors and conversion rates
  - SEO Stats: Monitor search engine rankings
  - Messages/Chatbots: Interact with patients
  - Online Reputation Manager: Manage patient reviews
  - Website Editor: Make changes to the website
  - Blog Manager: Review and edit blog posts
  - Social Media Post Management: Manage social media posts
  - Profile Settings: Update profile information

- **Patient Check-in App:**
  - Check-in: Patients can check in on arrival
  - Check-in Confirmation: Display confirmation message

## Project Features

### Authentication
- User signup with role selection
- Secure login with JWT
- Password reset functionality

### Practitioner Dashboard
- **Appointments Calendar:** Integrated with an appointment booking widget
- **Practice Analytics:**
  - Monthly patient acquisition stats
  - First-time appointments booked
  - Follow-up appointments booked
  - Appointments cancelled
- **Revenue Stats:** Monthly revenue generation
- **Website Analytics:**
  - Visitor stats (direct, organic search, ads, referral, other)
  - Conversion rate (% of website visitors that booked appointments)
- **SEO Stats:** Search rankings for targeted keywords
- **Messages/Chatbots:** Interact with patients via chat
- **Online Reputation Manager:** Manage and respond to online reviews
- **Website Editor:** Make changes to the practitioner's website
- **Blog Manager:** Review and edit blog posts
- **Social Media Management:** Manage and edit social media posts
- **Profile Settings:** Update practitioner's profile

### Patient Check-in App
- **Check-in:** Patients can check in using a tablet at the clinic
- **Check-in Confirmation:** Display a customizable message after check-in
- **Notification:** Practitioners receive text and email notifications when a patient checks in
