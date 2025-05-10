## Team Roles

In the development of the Airbnb Clone Project, the following roles contribute to building and maintaining the application:

### 1. Backend Developer
Responsible for building the server-side logic of the application. They create APIs, manage user authentication, and ensure smooth communication between the database and frontend. Technologies used often include Python (Flask or Django).

### 2. Frontend Developer
Focuses on the user interface and user experience. They implement responsive layouts, interactive components, and ensure that the platform is visually appealing and intuitive. Technologies include HTML, CSS, and JavaScript.

### 3. Database Administrator (DBA)
Designs and manages the database system. They are responsible for optimizing queries, ensuring data integrity, and implementing data backup and security policies.

### 4. DevOps Engineer
Handles deployment, CI/CD pipelines, and server management. They ensure the application runs efficiently in different environments and manage cloud infrastructure if needed.

### 5. UI/UX Designer
Designs user-friendly and visually appealing interfaces. They conduct user research, create wireframes/prototypes, and collaborate closely with frontend developers to ensure design consistency.

### 6. Project Manager
Oversees the entire project. They define timelines, coordinate between team members, manage tasks and milestones, and ensure the project goals are met efficiently.

### 7. Quality Assurance (QA) Engineer
Tests the application to identify bugs or usability issues. They ensure that the product meets the required standards before it goes live.

### 8. Product Owner
Defines the vision and requirements of the project. They act as the link between the client/stakeholders and the development team, prioritizing features based on business value.

## Technology Stack

The Airbnb Clone project uses a modern and scalable set of technologies to support both frontend and backend development. Below is a list of the core technologies and their roles in the project:

### 1. Django
A high-level Python web framework used to build robust and scalable backend APIs quickly. Django helps manage the application logic, user authentication, routing, and admin interface.

### 2. PostgreSQL
A powerful open-source relational database system used to store structured data such as users, listings, bookings, and reviews.

### 3. GraphQL
A query language for APIs that enables clients to request exactly the data they need. It helps improve frontend performance by minimizing over-fetching.

### 4. HTML/CSS/JavaScript
Used to build the user interface of the web application. HTML structures the content, CSS styles the layout, and JavaScript adds interactivity.

### 5. React.js (optional)
A JavaScript library for building fast, responsive, and component-based user interfaces. React can be used with GraphQL to manage UI rendering efficiently.

### 6. Git & GitHub
Used for version control and collaboration. Git tracks code changes, while GitHub hosts the codebase and supports team collaboration.

### 7. Docker (optional)
Containerization tool that ensures the application runs consistently across different environments by packaging dependencies together.


## Database Design

The database schema is designed to support the core functionalities of an Airbnb-like platform. Below are the main entities, their key fields, and relationships:

### 1. Users
Represents all users of the platform, including hosts and guests.

- `id` (Primary Key)
- `name`
- `email`
- `password_hash`
- `is_host` (Boolean to identify hosts)

**Relationships**:
- A user can create multiple properties.
- A user can make multiple bookings.
- A user can write multiple reviews.

---

### 2. Properties
Represents the accommodations listed by hosts.

- `id` (Primary Key)
- `title`
- `description`
- `location`
- `price_per_night`
- `host_id` (Foreign Key to Users)

**Relationships**:
- A property belongs to one host (user).
- A property can have multiple bookings and reviews.

---

### 3. Bookings
Represents reservation data for guests.

- `id` (Primary Key)
- `user_id` (Foreign Key to Users)
- `property_id` (Foreign Key to Properties)
- `start_date`
- `end_date`

**Relationships**:
- A booking belongs to one user and one property.

---

### 4. Reviews
Stores feedback left by users after a stay.

- `id` (Primary Key)
- `user_id` (Foreign Key to Users)
- `property_id` (Foreign Key to Properties)
- `rating` (1 to 5)
- `comment`

**Relationships**:
- A review belongs to one user and one property.

---

### 5. Payments
Tracks transactions made for bookings.

- `id` (Primary Key)
- `booking_id` (Foreign Key to Bookings)
- `amount`
- `payment_date`
- `payment_method`

**Relationships**:
- A payment is linked to a specific booking.




