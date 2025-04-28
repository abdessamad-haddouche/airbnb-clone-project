# Airbnb Clone Project

## Project Overview
The **Airbnb Clone Project** is a real-world application designed to simulate the development of a scalable booking platform similar to Airbnb.  
It involves building the backend systems, designing a relational database, developing secure APIs, and integrating modern deployment practices.  

## Project Goals
- Develop a robust backend system for a property booking platform.
- Apply modern software development practices, including CI/CD, security, and scalable architecture.
- Master database schema design and relational data modeling.
- Implement secure APIs following industry standards.
- Simulate real-world team collaboration and documentation practices.

## Team Roles

Effective execution of the Airbnb Clone Project involves collaboration across several key roles.

### Backend Developer
The Backend Developer is responsible for building and maintaining the server-side logic of the application. They design RESTful and GraphQL APIs, integrate the database with the application, implement authentication mechanisms, and ensure overall performance, scalability, and security of the backend services.

### Database Administrator (DBA)
The Database Administrator oversees the design, implementation, and maintenance of the relational database. Their responsibilities include modeling the database schema, ensuring data integrity and availability, optimizing queries for performance, and implementing database security measures.

### DevOps Engineer
The DevOps Engineer is tasked with automating the development, testing, and deployment processes. They set up CI/CD pipelines using tools like GitHub Actions and Docker, manage production and development environments, and ensure system reliability through monitoring and automated recovery processes.

### Security Engineer
The Security Engineer focuses on safeguarding the application against vulnerabilities. They implement authentication and authorization protocols, secure API endpoints, enforce best practices in data protection, and conduct regular security audits to identify and mitigate potential risks.

### Project Manager
The Project Manager coordinates all aspects of the project development lifecycle. They are responsible for setting milestones, facilitating communication between team members, managing task assignments, monitoring progress, and ensuring that the project goals and deadlines are achieved.

### QA Engineer
The Quality Assurance (QA) Engineer ensures that the application functions as intended. They create and execute test plans, perform manual and automated testing, report bugs, and validate that all features meet the specified requirements before release.

## Technology Stack
- **Django**: Web framework for backend development and API management.
- **MySQL**: Relational database system for managing structured application data.
- **GraphQL**: API query language for efficient client-server interactions.
- **Docker**: Containerization tool for consistent development and deployment environments.
- **GitHub Actions**: CI/CD tool for automating testing, building, and deployment processes.

## Database Design

The database for the Airbnb Clone Project is structured around several key entities to support core functionalities like user management, property listings, bookings, reviews, and payment processing.

### Users
- **id**: Unique identifier for each user.
- **name**: Full name of the user.
- **email**: Email address used for login and communication.
- **password_hash**: Securely stored password information.
- **role**: Indicates whether the user is a host or a guest.

### Properties
- **id**: Unique identifier for each property.
- **owner_id**: Foreign key referencing the user (host) who owns the property.
- **title**: Name or title of the property listing.
- **description**: Detailed description of the property.
- **location**: Physical address or geographical location of the property.

### Bookings
- **id**: Unique identifier for each booking.
- **property_id**: Foreign key referencing the booked property.
- **user_id**: Foreign key referencing the guest who made the booking.
- **start_date**: Check-in date.
- **end_date**: Check-out date.

### Reviews
- **id**: Unique identifier for each review.
- **property_id**: Foreign key referencing the reviewed property.
- **user_id**: Foreign key referencing the guest who wrote the review.
- **rating**: Numeric score reflecting the user’s satisfaction.
- **comment**: Textual feedback left by the user.

### Payments
- **id**: Unique identifier for each payment transaction.
- **user_id**: Foreign key referencing the guest who made the payment.
- **booking_id**: Foreign key referencing the associated booking.
- **amount**: Total amount paid for the booking.
- **payment_status**: Indicates whether the payment was successful, pending, or failed.

### Entity Relationships
- A **User** can own multiple **Properties**.
- A **User** (guest) can make multiple **Bookings**.
- Each **Booking** is linked to one **Property** and one **User**.
- A **User** can leave multiple **Reviews** for different **Properties**.
- A **Payment** is associated with a **Booking** and the corresponding **User**.

