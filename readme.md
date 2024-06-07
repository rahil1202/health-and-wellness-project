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



# Project Design

## System Architecture
   ![image](https://github.com/rahil1202/health-and-wellness-project/assets/104057403/8d070c13-2acf-425b-8a32-3797ff3c9df2)


## Component Diagram
![image](https://github.com/rahil1202/health-and-wellness-project/assets/104057403/83cfad02-2e26-4392-8457-cc1801884772)


## Database Schema
![image](https://github.com/rahil1202/health-and-wellness-project/assets/104057403/8b179add-cfc2-40fd-9511-e0983911801d)


## User Authentication Flow
![image](https://github.com/rahil1202/health-and-wellness-project/assets/104057403/c0a4df90-d54d-4a72-bfec-3adad0414e8c)


## Appointment Booking Flow
![image](https://github.com/rahil1202/health-and-wellness-project/assets/104057403/d1d5ab3b-60b9-416c-90c0-d8440c77040f)


## Patient Check-in Flow
![image](https://github.com/rahil1202/health-and-wellness-project/assets/104057403/0ead7c1a-ccb3-4f23-bf6b-c783139d8fcd)


## Analytics Processing Flow
![image](https://github.com/rahil1202/health-and-wellness-project/assets/104057403/9883a61c-02ea-498d-9043-a4bcaf4beb3c)


## Online Reputation Management Flow
![image](https://github.com/rahil1202/health-and-wellness-project/assets/104057403/df6e8cb7-66d8-4da5-8489-850c905aac54)



## High-Level System Design

### Architecture

The platform follows a typical client-server architecture with the following components:

1. **Frontend (Client):** A React.js application that provides an interactive user interface for practitioners and patients. The frontend communicates with the backend via RESTful APIs.

2. **Backend (Server):** A Java Spring Boot application that handles business logic, processes requests from the frontend, and interacts with the database.

3. **Database:** A MySQL relational database that stores all persistent data related to practitioners, patients, appointments, analytics, and more.


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
