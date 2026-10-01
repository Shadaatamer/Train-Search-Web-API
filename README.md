rain Search Web API
A RESTful Train Search Web API developed as part of an Enozom technical task.
The project is built with ASP.NET Core (.NET 8) and follows a layered architecture to keep the API, business logic, domain models, and data-access responsibilities separated.
Overview
The API is designed to support train/trip search functionality while demonstrating clean backend structure, dependency injection, repository/service separation, and database integration.
Tech Stack
- .NET 8
- ASP.NET Core Web API
- Entity Framework Core 8
- MySQL
- Pomelo Entity Framework Core MySQL Provider
- Swagger / OpenAPI
- Dependency Injection
- Repository & Service Pattern
Project Structure
Train-Search-Web-API/
│
├── Controllers/                  # API controllers
├── EnozomTask.Application/      # Application services, interfaces and use cases
├── EnozomTask.Domain/           # Domain entities and core models
├── EnozomTask.Infrastructure/   # Database context and repository implementations
├── Properties/                  # Application launch settings
├── Program.cs                   # Application configuration and DI registration
├── EnozomTask.csproj            # Main Web API project
└── EnozomTask.sln               # Solution file
Architecture
The solution separates responsibilities into the following layers:
- API / Controllers – receives HTTP requests and returns API responses.
- Application – contains business services and repository abstractions.
- Domain – contains the core domain models.
- Infrastructure – contains Entity Framework Core, MySQL access, and repository implementations.
The application registers the trip repository and service through ASP.NET Core dependency injection.
Getting Started
Prerequisites
Make sure you have installed:
- .NET 8 SDK
- MySQL Server
- Visual Studio 2022, JetBrains Rider, or VS Code (optional)
1. Clone the repository
git clone https://github.com/Shadaatamer/Train-Search-Web-API.git
cd Train-Search-Web-API
2. Restore dependencies
dotnet restore
3. Configure the database
Add a DefaultConnection connection string to your local configuration, for example in appsettings.json or using .NET user secrets.
Example:
{
  "ConnectionStrings": {
    "DefaultConnection": "Server=localhost;Database=EnozomTaskDb;User=root;Password=your_password;"
  }
}
Do not commit real database credentials to source control.

4. Run the application
dotnet run
The development profile can be accessed locally based on the URL shown in the terminal when the application starts.
Swagger / API Testing
Swagger is enabled in the Development environment.
After starting the project, open the Swagger URL shown by the application, typically similar to:
https://localhost:<port>/swagger
Swagger can be used to inspect and test the available API endpoints directly from the browser.
Main Concepts Demonstrated
- REST API development with ASP.NET Core
- Clean separation of concerns
- Repository pattern
- Service layer
- Dependency injection
- Entity Framework Core integration
- MySQL database connectivity
- Swagger/OpenAPI documentation
Technical Task
This repository was created as an Enozom technical assessment/task to demonstrate backend development skills using ASP.NET Core, Entity Framework Core, MySQL, and a structured application architecture.
