# Mechanic Shop Management System

A full-stack mechanic shop management platform built with **.NET Core Web API**, **Clean Architecture**, and **Blazor WebAssembly (WASM)**.

This solution provides a scalable and maintainable architecture for managing customers, vehicles, repair jobs, invoices, inventory, appointments, and workshop operations.

---

# 🚀 Technologies Used

## Backend
- ASP.NET Core Web API
- Clean Architecture
- Entity Framework Core
- SQL Server
- MediatR
- FluentValidation
- AutoMapper
- JWT Authentication
- Serilog Logging

## Frontend
- Blazor WebAssembly (WASM)
- MudBlazor / Bootstrap UI
- REST API Integration
- Authentication & Authorization

## DevOps & Tools
- Docker
- Swagger / OpenAPI
- GitHub Actions (Optional)
- xUnit / NUnit Testing

---

# 📁 Solution Structure

```bash
Mechanic-Shop/
│
├── src/
│
│   ├── Core/
│   │   ├── MechanicShop.Domain/
│   │   │   ├── Entities/
│   │   │   ├── ValueObjects/
│   │   │   ├── Enums/
│   │   │   ├── Events/
│   │   │   └── Interfaces/
│   │   │
│   │   └── MechanicShop.Application/
│   │       ├── Features/              # CQRS (Commands & Queries)
│   │       ├── DTOs/
│   │       ├── Interfaces/
│   │       ├── Validators/
│   │       └── Common/
│
│   ├── Infrastructure/
│   │   ├── MechanicShop.Infrastructure/
│   │   │   ├── Persistence/          # DbContext, Configurations, Migrations
│   │   │   ├── Identity/             # Authentication & Authorization
│   │   │   ├── Services/             # External services (Email, Files, etc.)
│   │   │   └── Repositories/
│
│   ├── Presentation/
│   │   ├── MechanicShop.API/
│   │   │   ├── Controllers/
│   │   │   ├── Middleware/
│   │   │   ├── Extensions/
│   │   │   └── Program.cs
│   │   │
│   │   └── MechanicShop.BlazorWasm/
│   │       ├── Pages/
│   │       ├── Components/
│   │       ├── Services/
│   │       ├── Shared/
│   │       └── wwwroot/
│
├── tests/
│   ├── UnitTests/
│   ├── IntegrationTests/
│
├── docker/
├── docs/
├── .github/
├── appsettings.json
├── docker-compose.yml
└── README.md
```

# 🧱 Clean Architecture Layers

## Domain Layer
Contains:
- Entities
- Enums
- Value Objects
- Domain Events
- Business Rules

No external dependencies.

---

## Application Layer
Contains:
- CQRS Commands & Queries
- DTOs
- Validators
- Interfaces
- Business Logic

Uses:
- MediatR
- FluentValidation

---

## Infrastructure Layer
Contains:
- Database Context
- Repository Implementations
- Identity Services
- External Integrations
- Logging

Uses:
- Entity Framework Core
- SQL Server

---

## Presentation Layer

### API
Responsible for:
- REST Endpoints
- Authentication
- Swagger Documentation
- Middleware

### Blazor WASM
Responsible for:
- UI Components
- Client-side State Management
- API Consumption
- Authentication Flow

---

# ✨ Features

- Customer Management
- Vehicle Management
- Mechanic Management
- Service Orders
- Repair Tracking
- Appointment Scheduling
- Invoice Generation
- Inventory & Parts Management
- Authentication & Authorization
- Dashboard & Reports
- Responsive UI

---

# 🔐 Authentication

Authentication is implemented using JWT Bearer Tokens.

Roles supported:
- Admin
- Mechanic
- Receptionist
- Customer

---

# ⚙️ Getting Started

# Prerequisites

Make sure you have installed:

- .NET SDK 8.0+
- SQL Server
- Visual Studio 2022 / VS Code
- Node.js (optional)

---

# 🛠️ Setup Instructions

## 1. Clone Repository

```bash
git clone https://github.com/yourusername/mechanic-shop-system.git

cd mechanic-shop-system
```

---

## 2. Configure Database

Update connection string inside:

```bash
src/Presentation/API/appsettings.json
```

Example:

```json
"ConnectionStrings": {
  "DefaultConnection": "Server=.;Database=MechanicShopDb;Trusted_Connection=True;TrustServerCertificate=True"
}
```

---

## 3. Apply Migrations

```bash
dotnet ef database update \
--project src/Infrastructure/Persistence \
--startup-project src/Presentation/API
```

---

## 4. Run API

```bash
cd src/Presentation/API

dotnet run
```

API URL:

```bash
https://localhost:5001
```

Swagger:

```bash
https://localhost:5001/swagger
```

---

## 5. Run Blazor WASM

```bash
cd src/Presentation/BlazorWasm

dotnet run
```

Frontend URL:

```bash
https://localhost:7001
```

---

# 🧪 Running Tests

```bash
dotnet test
```

---

# 🐳 Docker Support

## Build Docker Containers

```bash
docker-compose up --build
```

---

# 📦 API Modules

## Customers
- Create Customer
- Update Customer
- Customer History

## Vehicles
- Register Vehicle
- Service History
- VIN Tracking

## Work Orders
- Assign Mechanics
- Track Status
- Update Repair Notes

## Inventory
- Manage Parts
- Stock Tracking
- Supplier Records

## Billing
- Generate Invoices
- Payment Tracking

---

# 📊 Future Improvements

- Real-time Notifications (SignalR)
- Mobile Application
- Online Booking
- SMS & Email Notifications
- AI-based Maintenance Suggestions

---

# 🔧 Design Principles

- SOLID Principles
- Separation of Concerns
- Dependency Injection
- CQRS Pattern
- Repository Pattern
- Clean Code Practices

---

# 🤝 Contributing

1. Fork the repository

2. Create feature branch

```bash
git checkout -b feature/your-feature
```

3. Commit changes

```bash
git commit -m "Add new feature"
```

4. Push branch

```bash
git push origin feature/your-feature
```

5. Open Pull Request

---

# 📝 License

This project is licensed under the MIT License.

---

# 👨‍💻 Author

Developed with .NET Clean Architecture & Blazor WebAssembly.