# Train Search Web API

A RESTful Web API developed using **ASP.NET Core .NET 8** as part of the **Enozom Technical Task**.

The project follows a clean layered architecture and provides backend functionality for searching and managing train-related data.

## Technical Task

This project was developed as a technical assessment for **Enozom** to demonstrate backend development skills, API design, database integration, clean architecture, and code organization using ASP.NET Core.

## Technologies Used

- ASP.NET Core Web API
- .NET 8
- C#
- Entity Framework Core
- MySQL
- Swagger / OpenAPI
- Dependency Injection

## Project Architecture

The solution is organized into multiple layers to maintain separation of concerns:

```text
Train-Search-Web-API
│
├── API
├── Application
├── Domain
└── Infrastructure
```

### API Layer

Responsible for:

- API Controllers
- HTTP Requests and Responses
- Swagger configuration
- Application startup and dependency configuration

### Application Layer

Contains the application logic and coordinates communication between the API and domain layers.

### Domain Layer

Contains the core business entities and domain models.

### Infrastructure Layer

Responsible for external resources such as:

- Database access
- Entity Framework Core
- MySQL configuration
- Repository / persistence implementation

## Getting Started

### Prerequisites

Make sure you have the following installed:

- .NET 8 SDK
- MySQL Server
- Visual Studio / Visual Studio Code / JetBrains Rider

## Clone the Repository

```bash
git clone https://github.com/Shadaatamer/Train-Search-Web-API.git
```

Navigate to the project directory:

```bash
cd Train-Search-Web-API
```

## Database Configuration

Update the database connection string inside the project configuration file:

```json
{
  "ConnectionStrings": {
    "DefaultConnection": "server=localhost;database=TrainSearchDB;user=root;password=your_password"
  }
}
```

Replace the database credentials with your local MySQL configuration.

## Restore Dependencies

Run:

```bash
dotnet restore
```

## Run the Application

Use:

```bash
dotnet run
```

After starting the application, the API will be available through the configured localhost URL.

## Swagger

Swagger is included for testing and documenting the API endpoints.

After running the application, open:

```text
https://localhost:<port>/swagger
```

Swagger allows you to:

- View available API endpoints
- Test API requests
- Review request parameters
- Inspect API responses

## Key Concepts Demonstrated

This technical task demonstrates:

- RESTful API development
- ASP.NET Core Web API
- Clean and layered architecture
- Entity Framework Core
- MySQL database integration
- Dependency Injection
- Separation of concerns
- API documentation using Swagger
- Maintainable backend project structure

## Repository

GitHub:

https://github.com/Shadaatamer/Train-Search-Web-API

## Author

Developed as part of the **Enozom Technical Task**.
