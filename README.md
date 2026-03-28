Mini Auth Service

A lightweight authentication microservice built with ASP.NET Core, providing JWT-based authentication, user registration, and secure token handling.
This project is designed as a beginner-friendly introduction to authentication in microservice architecture.

Features
User Registration
User Login
JWT Token Generation
Protected API Endpoints
Password Hashing & Security
Simple and clean architecture

Tech Stack
Backend: ASP.NET Core Web API
Authentication: JWT (JSON Web Token)
Database: SQLite 
ORM: Entity Framework Core



Setup Instructions

1. Clone the repository
git clone https://github.com/sahannadiranga-source/auth-microservice.git
2. Navigate to the project
cd mini-auth-service
3. Configure Database

Update your connection string in appsettings.json:

"ConnectionStrings": {
  "DefaultConnection": "your_connection_string_here"
}

4. Run Migrations (if using EF Core)
dotnet ef database update
5. Run the application
dotnet run

Authentication Flow
User registers with username & password
Password is hashed and stored securely
User logs in with credentials
Server validates and generates JWT token
Token is used to access protected endpoints

API Endpoints

Auth
POST /api/auth/register
Register a new user

POST /api/auth/login
Authenticate user and return JWT token

Protected Example
GET /api/secure-data
Requires valid JWT token

Example Request (Login)
POST /api/auth/login
Content-Type: application/json
{
  "username": "testuser",
  "password": "password123"
}

Future Improvements
Role-based authorization
Refresh tokens
OAuth integration (Google, GitHub)
Docker support
CI/CD pipeline
API Gateway integration

