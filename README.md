# Enterprise CRM System – Frontend (Angular)

Frontend application developed with Angular for an enterprise CRM system focused on inventory management, workforce control, operational scheduling, and performance analytics.

This application consumes a secure REST API deployed in Microsoft Azure and implements JWT-based authentication with Role-Based Access Control (RBAC). It also includes advanced business logic for report generation and workforce data consolidation.

---

## 🚀 Features

- JWT-based authentication
- Role-based access control (Admin / User)
- Protected routes using Angular Guards
- HTTP Interceptor for automatic token injection
- Inventory management (CRUD)
- Inventory movement tracking (inbound / outbound)
- Workforce and project management
- Schedule and attendance control
- Productivity and performance metrics
- Automated Excel report generation
- CI/CD deployment with Azure Static Web Apps
- Responsive desktop-oriented UI

---

## 📊 Advanced Reporting Module

The system includes a dynamic Excel report generation module built using:

- `xlsx`
- `file-saver`
- RxJS (`forkJoin` for multi-source data consolidation)

### Business Logic Implemented

The reporting service:

- Aggregates data from multiple services simultaneously
- Consolidates:
  - Workday records
  - Additional time entries
  - Absenteeism records
- Filters by date range, location, and employees
- Handles shifts crossing midnight
- Automatically classifies absence types:
  - Incapacity
  - General illness
  - Leave
  - Suspension
  - Unjustified absence
- Calculates:
  - Total worked hours
  - Overtime (+25%)
  - Night hours (+35%)
  - Sunday/Festive bonuses (+75%)
- Sorts records chronologically
- Generates one Excel sheet per employee
- Produces structured, analysis-ready reports

This module demonstrates advanced data normalization, transformation, and enterprise-level business rule implementation.

---

## 🏗 Architecture

The project follows a scalable enterprise-oriented architecture using Angular Standalone APIs:

- Standalone bootstrap (`bootstrapApplication`)
- `provideRouter()` for routing
- `provideHttpClient()` for API communication
- Modular feature-based organization
- Separation of concerns (components, services, models)
- Centralized API layer
- Route protection via:
  - `authGuard`
  - `adminGuard`
- Environment-based configuration
- Local storage session management
- Token decoding using `jwt-decode`

The structure ensures maintainability, scalability, and enterprise readiness.

---

## 🔐 Authentication & Security

- Login system using JWT
- Token decoding to extract:
  - User name
  - Role
  - Assigned project (obra)
- Role-based access control (RBAC)
- Protected routes using Guards
- Secure communication with Azure-hosted backend
- Session persistence via LocalStorage
- Automatic token injection in HTTP requests

---

## ☁ CI/CD & Deployment

The frontend is automatically deployed using:

- GitHub Actions
- Azure Static Web Apps

### Pipeline Features

- Trigger on push to `main`
- Automatic build using:
  - `npm ci`
  - `npm run build`
- Secure deployment via GitHub Secrets
- Pull request validation workflow

This ensures continuous integration and continuous deployment aligned with enterprise DevOps practices.

---

## 🌐 Backend Integration

This frontend consumes a REST API developed in ASP.NET Core and deployed in Microsoft Azure.

The API provides endpoints for:

- Authentication
- Inventory management
- Workforce management
- Time tracking
- Metrics and performance data

API base URL configuration:

src/environments/environment.ts


---

## 🛠 Tech Stack

- Angular 19 (Standalone Architecture)
- TypeScript
- RxJS
- Bootstrap / CSS
- XLSX (Excel generation)
- file-saver
- JWT Authentication
- Azure Static Web Apps
- GitHub Actions (CI/CD)
- REST API integration (ASP.NET Core backend)

---

## ⚙ Development Setup

Install dependencies:

```bash
npm install

Run development server:

ng serve
```

Navigate to:

```bash
http://localhost:4200/
📦 Production Build
ng build --configuration=production

Build artifacts are generated in the dist/ directory.
```

📌 Author

Carlos Lafaurie
Full Stack Developer – Angular & .NET
