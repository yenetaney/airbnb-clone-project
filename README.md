# Airbnb Clone Backend
The backend for the Airbnb Clone project is built to provide a scalable and efficient system for managing users, properties, bookings, and payments. It aims to replicate core features of Airbnb while ensuring secure transactions, optimized data handling, and a seamless user experience.
# Key Features
- User Management – Secure authentication and profile management.
- Property Listings – Creation, updates, and retrieval of rental properties.
- Booking System – Reservation and booking management.
- Payment Integration – Handling secure transactions.
- Review System – User-generated ratings and feedback.
## Team Roles
- Backend Developer: Responsible for implementing API endpoints, database schemas, and business logic.
- Database Administrator: Manages database design, indexing, and optimizations.
- DevOps Engineer: Handles deployment, monitoring, and scaling of the backend services.
- QA Engineer: Ensures the backend functionalities are thoroughly tested and meet quality standards.
# Technology Stack
- Django: A high-level Python web framework used for building the RESTful API.
- Django REST Framework: Provides tools for creating and managing RESTful APIs.
- PostgreSQL: A powerful relational database used for data storage.
- GraphQL: Allows for flexible and efficient querying of data.
- Celery: For handling asynchronous tasks such as sending notifications or processing payments.
- Redis: Used for caching and session management.
- Docker: Containerization tool for consistent development and deployment environments.
- CI/CD Pipelines: Automated pipelines for testing and deploying code changes.
## Database Design  

Each entity in the backend is designed to maintain structured relationships to ensure efficient data management. Below is an overview of how they connect:  

### 🔹 User & Property  
- A **User** (host) can list **multiple Properties**.  
- Each **Property** is owned by **one host (User)**.  

### 🔹 Property & Booking  
- A **guest (User)** can book a **Property**.  
- A **Property** can have **multiple Bookings** from different users.  
- Each **Booking** belongs to **one specific Property**.  

### 🔹 User & Booking  
- A **guest (User)** can make **multiple Bookings**.  
- A **Booking** belongs to **one guest (User)**.  
- A **host (User)** can have **multiple Bookings** for their listed Properties.  

### 🔹 Booking & Payment  
- Each **Booking** is linked to **one Payment**.  
- A **guest (User)** makes the **Payment** for the booking.  
- A **Payment** belongs to **one specific Booking**.  

### 🔹 User & Review  
- A **guest** can leave **one Review** per **Property** they booked.  
- A **Property** can have **multiple Reviews** from different guests.  
- A **Review** is linked to **one Property** and **one User**.  













