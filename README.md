# Enterprise CRM System – Frontend (Angular)

Frontend application developed with Angular for an enterprise CRM system focused on inventory management, movement tracking, schedule control, and operational performance metrics.

This application consumes a secure REST API deployed in Azure and implements authentication using JWT with role-based access control (RBAC).

---

## 🚀 Features

- User authentication (JWT-based)
- Role-based access control (Admin / User)
- Inventory management (CRUD)
- Inventory movement tracking (inbound / outbound)
- Schedule management
- Dashboard with operational metrics (KPIs)
- Protected routes using Angular Guards
- HTTP Interceptors for token handling
- Responsive design for desktop environments

---

## 🏗 Architecture

The project follows a modular feature-based architecture:

- Separation of concerns (components, services, models)
- Lazy-loaded modules
- Centralized API service layer
- Route protection via Guards
- HTTP Interceptor for JWT token injection
- Environment-based configuration

The application is structured to ensure scalability and maintainability in enterprise environments.

---

## 🛠 Tech Stack

- Angular 19
- TypeScript
- RxJS
- Bootstrap / CSS
- REST API integration
- JWT Authentication
- Azure-hosted backend

---

## 🔐 Authentication & Security

- Login system using JWT
- Token storage and automatic injection via HTTP Interceptor
- Route protection based on user roles
- Secure communication with Azure-hosted backend API

---

## 🌐 Backend Integration

This frontend consumes a REST API developed in ASP.NET Core and deployed in Azure.

API Base URL is configured in:

src/environments/environment.ts


---

## ⚙ Development Setup

Install dependencies:

```bash
npm install

Run development server:

ng serve

Navigate to:

http://localhost:4200/
📦 Production Build
ng build --configuration=production

Build artifacts are stored in the dist/ directory.

☁ Deployment

The backend API is deployed in Microsoft Azure.

Frontend can be deployed using:

Azure Static Web Apps

Azure App Service

Any static hosting provider

📌 Author

Carlos Lafaurie
Full Stack Developer – Angular & .NET
