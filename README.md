About the Project
The Airbnb Clone Project is a comprehensive, real-world application designed to simulate the development of a robust booking platform like Airbnb. It involves a deep dive into full-stack development, focusing on backend systems, database design, API development, and application security. This project enables learners to understand complex architectures, workflows, and collaborative team dynamics while building a scalable web application.

Learning Objective
This project is tailored to enhance your expertise in modern software development practices. By completing these tasks, learners will:

Master collaborative team workflows using GitHub.
Deepen their understanding of backend architecture and database design principles.
Implement advanced security measures for API development.
Gain proficiency in designing and managing CI/CD pipelines for efficient deployment.
Strengthen their ability to document and plan complex software projects effectively.
Develop an understanding of integrating technologies like Django, MySQL, and GraphQL in a unified ecosystem.
Requirements
To successfully complete the project tasks, learners must:

Have a GitHub account to create and manage repositories.
Be familiar with Markdown syntax for README.md file creation.
Possess prior experience with backend frameworks like Django and database systems such as MySQL.
Understand software development lifecycle practices, including security, CI/CD, and database design.
Be comfortable with modern tools such as Docker, GitHub Actions, or similar CI/CD platforms.
Key Highlights
Hands-on GitHub Repository Management:
Learn to initialize and structure a project repository, adhering to industry best practices.

Team Role Documentation:
Understand and articulate the responsibilities of various team members, fostering collaboration in real-world scenarios.

Technology Stack Breakdown:
Explore the technologies used in a scalable project and their specific contributions to achieving project goals.

Database Design Proficiency:
Plan and document a relational database structure with entities, attributes, and relationships that mirror real-world requirements.

Feature-Driven Development:
Identify and describe core features of the application, focusing on their relevance to the user experience and business logic.

API Security Fundamentals:
Implement and document key security measures to safeguard application data and ensure secure transactions.

CI/CD Pipeline Integration:
Gain insights into setting up automated development pipelines, boosting efficiency and minimizing errors during the deployment phase.

This structured approach ensures learners not only build technical skills but also adopt a mindset geared toward problem-solving, scalability, and industry-grade project execution.

## 🗃️ Database Design
### 1. Users
- Fields:
  - `id`: Unique identifier
  - `username`: The user’s login name
  - `email`: Contact email
  - `is_host`: Boolean to check if user can list properties
  - `bio`: Short user profile text
- Relationships:
  - One user can create many properties
  - One user can make many bookings
  - One user can leave many reviews

---

### 2. Properties
- Fields:
  - `id`: Unique property ID
  - `owner`: Linked to the user who created the listing
  - `title`: Property name
  - `description`: Detailed info about the property
  - `price`: Cost per night
- Relationships:
  - Each property belongs to one user (host)
  - One property can have many bookings
  - One property can receive many reviews

---

### 3. Bookings
- Fields:
  - `id`: Unique booking ID
  - `user`: The user who booked
  - `property`: The property being booked
  - `check_in`: Start date
  - `check_out`: End date
- Relationships:
  - Each booking is made by one user
  - Each booking is for one property
  - Each booking can have one payment

---

### 4. Payments
- Fields:
  - `id`: Unique payment ID
  - `booking`: The booking being paid for
  - `amount`: Total cost
  - `status`: Paid/failed/pending
  - `timestamp`: When payment was made
- Relationships:
  - Each payment is for one booking

---

### 5. Reviews
- Fields:
  - `id`: Unique review ID
  - `user`: Reviewer
  - `property`: Reviewed property
  - `rating`: Score from 1–5
  - `comment`: Written feedback
- Relationships:
  - One user can leave multiple reviews
  - One property can have multiple reviews
