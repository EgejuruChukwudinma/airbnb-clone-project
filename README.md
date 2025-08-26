Airbnb Clone Project – Backend

This project is a full-stack simulation of Airbnb’s core booking platform. The backend focuses on building robust APIs, managing a relational database, and implementing secure user and booking management workflows.

Project Goals
- Simulate a real-world backend development process
- Learn database design and backend architecture
- Build secure REST APIs and implement authentication
- Practice using CI/CD and deployment tools

Tech Stack
- Django (Backend Web Framework)
- MySQL or PostgreSQL (Relational Database)
- GraphQL (Optional API Layer)
- Git & GitHub
- Docker (Containerization)
- GitHub Actions (CI/CD)

Team Roles

| Role                  | Responsibilities |
|------------------------|------------------|
| Backend Developer     | Build RESTful APIs, define models, handle business logic |
| Database Administrator| Design and manage the relational database schema |
| DevOps Engineer       | Setup Docker, CI/CD pipelines, monitor server resources |
| API Security Engineer | Ensure APIs are secure (authentication, rate-limiting, data validation) |
| Technical Writer      | Maintain documentation for endpoints, setup guides, and architecture |

Technology Stack

| Technology     | Purpose in the Project |
|----------------|------------------------|
| **Django**     | Backend framework used to build APIs, manage models, and handle server logic |
| **MySQL**      | Relational database to store structured data such as users, properties, and bookings |
| **GraphQL**    | (Optional) API layer allowing flexible queries between client and server |
| **Docker**     | Containerizes the project for consistent deployment across machines |
| **GitHub Actions** | Automates testing and deployment processes (CI/CD) |
| **Git**        | Version control for team collaboration |

Database Design
 Key Entities and Fields

1. **Users**
   - `id` (PK)
   - `name`
   - `email`
   - `password_hash`
   - `role` (guest or host)

2. **Properties**
   - `id` (PK)
   - `host_id` (FK to Users)
   - `title`
   - `description`
   - `location`

3. **Bookings**
   - `id` (PK)
   - `user_id` (FK to Users)
   - `property_id` (FK to Properties)
   - `check_in`
   - `check_out`

4. **Reviews**
   - `id` (PK)
   - `user_id` (FK to Users)
   - `property_id` (FK to Properties)
   - `rating`
   - `comment`

5. **Payments**
   - `id` (PK)
   - `booking_id` (FK to Bookings)
   - `amount`
   - `status`
   - `payment_method`

### Relationships

- One **user** can have many **properties**.
- One **user** can make many **bookings**.
- Each **booking** is linked to one **property** and one **user**.
- Each **review** belongs to one user and one property.
- Each **payment** is linked to one booking.

Feature Breakdown

1. **User Authentication**
   - Handles user registration, login, and token-based authentication.

2. **Property Management**
   - Allows hosts to list, update, or remove properties.

3. **Booking System**
   - Enables guests to book properties and check availability.

4. **Payment Integration**
   - Secure processing of payments using third-party services (e.g., Stripe or Paystack).

5. **Review System**
   - Lets users review properties after staying.

6. **Admin Panel**
   - For internal management of listings, users, and complaints.

These features help simulate a fully functional booking platform with real-world workflows.
