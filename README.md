# Assignment Submission Portal

This project is a backend system for an assignment submission portal built with Spring Boot and MongoDB. The system supports two types of users: **Users** who can upload assignments and **Admins** who can manage these assignments.

## Features

- User registration and login.
- Admin registration and login.
- Users can upload assignments.
- Admins can view, accept, or reject assignments.

## Technologies Used

- **Spring Boot**: For building the REST API.
- **MongoDB**: NoSQL database for storing user and assignment data.
- **Spring Security**: For user authentication and authorization.
- **Lombok**: To reduce boilerplate code.

## Getting Started

### Prerequisites

- Java 17 or higher
- Maven
- MongoDB

User Endpoints
Register a new user

POST /users/register
Body:
json
Copy code
{
  "username": "exampleUser",
  "password": "examplePassword"
}
User login (to be implemented)

Admin Endpoints
Upload an assignment

POST /assignments/upload
Body:
json
Copy code
{
  "userId": "user_id",
  "task": "Task description",
  "adminId": "admin_id"
}
Get assignments for admin

GET /assignments/admin/{adminId}
Accept an assignment

POST /assignments/{id}/accept
Reject an assignment

POST /assignments/{id}/reject
