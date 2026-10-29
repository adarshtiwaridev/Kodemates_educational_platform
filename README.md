# 🎓 Kodemates EdTech

### Full-Stack Learning Management System (LMS)

A modern, full-stack Learning Management System built with the **MERN stack (MongoDB, Express.js, React, and Node.js)**. The platform provides an integrated learning environment for students, instructors, and administrators, combining course management, secure authentication, online payments, assessments, certificates, learning analytics, and AI-powered quiz generation.

Built with a focus on security, maintainability, scalability, and real-world learning workflows.

**Developed by:** Team Kodemates

**Repository:** [Edtech-projects](https://github.com/adarsh2027dev/Edtech-projects)

---

## 📌 Project Overview

Kodemates EdTech is designed to simplify online education by bringing learners, instructors, and administrators together in one platform.

Students can access courses, complete quizzes, track learning progress, participate in course discussions, and earn certificates. Instructors can manage courses and assess learners, while administrators can oversee platform activity and revenue analytics.

The platform combines traditional LMS functionality with additional capabilities such as PDF-to-quiz generation, multi-device session management, learning streaks, and certificate verification.

### 🎯 Project Objectives

* Provide a centralized online learning environment.
* Enable instructors to create and manage educational courses.
* Offer students structured learning and assessment workflows.
* Secure authentication and role-based authorization.
* Automate certificate generation and verification.
* Support online payments with server-side verification.
* Convert educational PDF notes into structured quizzes.
* Track learning activity and engagement.
* Provide analytics for platform administration and instructors.

---

## 🏷️ Technology Badges

[![MERN Stack](https://img.shields.io/badge/Stack-MERN-blue.svg)](https://github.com/adarsh2027dev/Edtech-projects)
[![Node.js](https://img.shields.io/badge/Node.js-%3E%3D18-green.svg)](https://nodejs.org/)
[![React](https://img.shields.io/badge/React-18.2.0-61DAFB.svg)](https://react.dev/)
[![Express](https://img.shields.io/badge/Express-4.21.2-black.svg)](https://expressjs.com/)
[![MongoDB](https://img.shields.io/badge/MongoDB-Atlas-47A248.svg)](https://www.mongodb.com/atlas)
[![Vite](https://img.shields.io/badge/Vite-Frontend-646CFF.svg)](https://vite.dev/)
[![Redux Toolkit](https://img.shields.io/badge/Redux_Toolkit-State_Management-764ABC.svg)](https://redux-toolkit.js.org/)
[![Razorpay](https://img.shields.io/badge/Payments-Razorpay-2B84EA.svg)](https://razorpay.com/)

---

## 🖼️ Application Screenshots

Explore the application's user interface through the following screenshots.

### 1. Learning Platform

![Kodemates EdTech Screenshot 1](https://github.com/user-attachments/assets/75804a93-22d0-404e-9fb1-11156c2eeea6)

### 2. Course and Learning Interface

![Kodemates EdTech Screenshot 2](https://github.com/user-attachments/assets/2ab9a242-9490-4224-945d-8bbfa43ca6b0)

### 3. Learning Dashboard

![Kodemates EdTech Screenshot 3](https://github.com/user-attachments/assets/acc5ac48-fa21-4ebe-931f-84d2238814fa)

### 4. Course Management Interface

![Kodemates EdTech Screenshot 4](https://github.com/user-attachments/assets/37104cf1-5b82-4b8d-8f41-32f269a02a13)

### 5. Additional Platform View

![Kodemates EdTech Screenshot 5](https://github.com/user-attachments/assets/cbb45262-b048-41d1-9c91-a3ffa8a3b9c7)

---

## ✨ Key Features

### 🔐 1. Secure Authentication and Session Management

The application implements JWT-based authentication with separate access and refresh tokens.

Features include:

* Short-lived access tokens.
* HTTP-only refresh-token cookies.
* Multi-device session tracking.
* Session-aware authentication.
* Protected routes and API endpoints.
* Role-based authorization.
* Account and session management.

The `StudentSession` model supports tracking active student sessions across devices.

**Security principle:** Authentication identifies the user, while authorization determines which operations the user may perform.

### 👨‍🎓 2. Student Learning Dashboard

The student experience focuses on course access, learning progress, assessments, and engagement.

Key capabilities include:

* Access to enrolled courses.
* Learning progress tracking.
* Quiz participation.
* Learning streak tracking.
* Certificate access.
* Course discussions.
* Skill-related analytics.
* Student activity tracking.

### 👨‍🏫 3. Instructor Course Management

Instructors can manage their educational content and monitor learner engagement.

The platform's course-management architecture supports workflows for:

* Course creation and management.
* Educational content organization.
* Course-related quizzes.
* Student learning activity.
* Course revenue analytics.
* Course discussion management.

Access to course operations should be restricted to authorized instructors and applicable administrators.

### 🛡️ 4. Administrative Dashboard

The administrative module provides platform-level management and analytics.

Its documented capabilities include:

* Platform revenue analytics.
* Administrative course and user workflows.
* Role-based access control.
* Platform activity visibility.
* Aggregated reporting.

### 🤖 5. AI-Powered PDF-to-Quiz Generation

The application includes a PDF quiz extraction service that combines document text extraction with Google Generative AI.

**Technology used:**

* `pdf-parse` for PDF text extraction.
* Google Generative AI for question generation.
* Zod for structured output validation.

#### Workflow

1. Educational material is provided as a PDF.
2. The backend extracts available text from the document.
3. The extracted content is passed through the configured quiz-generation workflow.
4. The AI generates candidate questions and answers.
5. The resulting structure is validated.
6. Validated quiz data can be used by the application's assessment workflow.

#### Benefits

* Reduces manual quiz preparation.
* Helps instructors generate assessments from course notes.
* Supports structured question generation.
* Connects educational resources with assessment workflows.

**Important:** AI-generated questions should be reviewed for factual accuracy, ambiguity, and alignment with the original material before being used in high-stakes assessments.

### 📜 6. Automated PDF Certificates

The platform generates PDF certificates using PDFKit.

Documented capabilities include:

* Server-side PDF generation.
* Unique UUID-based verification identifiers.
* Public certificate verification URLs.
* Certificate-related learning workflows.

#### Certificate Workflow

1. A learner satisfies the applicable completion requirements.
2. The backend validates eligibility.
3. A certificate is generated.
4. A unique verification identifier is associated with the certificate.
5. The certificate can be verified through its public verification endpoint.

Certificate verification should use server-side records rather than trusting information printed on a PDF alone.

### 🔥 7. Daily Learning Streaks

The learning streak engine records student activity and calculates consecutive learning days.

Features include:

* Daily activity tracking.
* Streak calculation.
* Learning engagement metrics.
* Streak recovery mechanisms.

The implementation should use consistent date boundaries and handle time zones correctly to avoid inaccurate streak calculations.

### 📊 8. Analytics and Reporting

The platform provides analytics tailored to different roles.

| Role       | Analytics Focus                                    |
| ---------- | -------------------------------------------------- |
| Student    | Learning progress and skill-related insights.      |
| Instructor | Course performance and revenue analytics.          |
| Admin      | Platform revenue and aggregated platform activity. |

MongoDB aggregations support the documented database and analytics architecture.

### 💳 9. Razorpay Payment Integration

Razorpay integration supports secure payment processing.

Documented capabilities include:

* Payment order creation.
* Checkout integration.
* Server-side payment signature verification.
* HMAC SHA-256 verification.
* Payment-related backend workflows.

#### Payment Verification

The backend verifies payment signatures using the appropriate Razorpay secret.

This helps prevent clients from falsely reporting successful payments.

The application should update enrollment or payment status only after successful server-side verification and appropriate payment-state validation.

### 💬 10. Course Discussion Forum

The platform includes course-level discussions to support collaborative learning.

Features include:

* Discussion questions.
* Nested answers.
* Upvoting.
* Course-associated conversations.

The backend should enforce authorization when creating, editing, or removing discussion content.

### 🧭 11. Protected Client-Side Routing

The React frontend uses React Router v6 with protected routing and role guards.

The frontend routing architecture includes:

* Authentication-aware routes.
* Protected pages.
* Role-based navigation.
* Restricted dashboard access.

Frontend route protection improves the user experience but must be backed by server-side authorization for every protected API.

---

## 🏛️ System Architecture

Kodemates EdTech uses a decoupled frontend and backend architecture.

The React frontend communicates with the Express REST API, which handles authentication, business logic, validation, database operations, and external service integrations.

### High-Level Architecture

```text
                   STUDENT / INSTRUCTOR / ADMIN
                               |
                               v
                  +---------------------------+
                  |       React 18 SPA        |
                  |       Vite                |
                  |       React Router        |
                  |       Redux Toolkit        |
                  |       Framer Motion        |
                  +-------------+-------------+
                                |
                                v
                  +---------------------------+
                  |       Axios API Client    |
                  | Access Token + Cookies    |
                  +-------------+-------------+
                                |
                                v
                  +---------------------------+
                  |    Node.js + Express      |
                  |       REST API            |
                  +-------------+-------------+
                                |
             +------------------+------------------+
             |                  |                  |
             v                  v                  v
    +----------------+ +------------------+ +----------------+
    | Authentication | | Course / Student | | Payment APIs   |
    | JWT / Sessions | | Quiz / Certificate| | Razorpay       |
    +----------------+ +------------------+ +----------------+
             |                  |                  |
             +------------------+------------------+
                                |
                                v
                  +---------------------------+
                  |      Service Layer        |
                  | Auth / Quiz / Student     |
                  | Certificate PDF Services  |
                  +-------------+-------------+
                                |
                                v
                  +---------------------------+
                  |       Mongoose ODM        |
                  | Models and Aggregations   |
                  +-------------+-------------+
                                |
                                v
                  +---------------------------+
                  |       MongoDB Atlas       |
                  +---------------------------+

       External Integrations:
       - Google Generative AI
       - Razorpay
       - Cloudinary
       - Email / Notification Services
```

### Architecture Principles

* Separate frontend presentation from backend business logic.
* Centralize authentication and authorization.
* Organize reusable business logic into services.
* Use Mongoose for schema-based data access.
* Validate incoming requests before processing them.
* Verify payment operations server-side.
* Keep secrets outside source code.
* Maintain consistent error handling.
* Test critical business workflows independently.

---

## 🛠️ Technology Stack

| Layer                    | Technology             | Purpose                                     |
| ------------------------ | ---------------------- | ------------------------------------------- |
| Frontend Framework       | React 18               | User interface development.                 |
| Frontend Build Tool      | Vite                   | Frontend development and production builds. |
| Client Routing           | React Router v6        | Navigation and protected routes.            |
| State Management         | Redux Toolkit          | Shared application state.                   |
| HTTP Client              | Axios                  | Communication with the REST API.            |
| UI Animation             | Framer Motion          | Interface animations and transitions.       |
| Backend Runtime          | Node.js                | JavaScript runtime.                         |
| Backend Framework        | Express.js 4           | REST API and middleware.                    |
| Database                 | MongoDB Atlas          | Persistent application data.                |
| ODM                      | Mongoose               | Database schemas and queries.               |
| Authentication           | JWT                    | Access-token authentication.                |
| Session Management       | StudentSession         | Active multi-device session tracking.       |
| Security Headers         | Helmet                 | HTTP security headers.                      |
| Rate Limiting            | express-rate-limit     | Request rate controls.                      |
| NoSQL Input Sanitization | express-mongo-sanitize | Mitigation for NoSQL injection patterns.    |
| File Upload              | Express File Upload    | File upload handling.                       |
| PDF Parsing              | pdf-parse              | Text extraction from PDF files.             |
| AI Integration           | Google Generative AI   | AI-assisted quiz generation.                |
| Schema Validation        | Zod                    | Structured data validation.                 |
| PDF Generation           | PDFKit                 | Server-side certificate generation.         |
| Payments                 | Razorpay               | Online payment processing.                  |
| Image Storage            | Cloudinary             | Image storage and delivery.                 |
| Backend Testing          | Jest                   | Unit and integration tests.                 |
| Frontend Testing         | Vitest                 | Frontend component and unit tests.          |

Package versions should be verified against the repository's current lockfiles.

---

## 📂 Repository Structure

The repository is organized into separate frontend and backend applications.

```text
Edtech-projects/
│
├── backend/
│   ├── src/
│   │   ├── config/
│   │   │   ├── Database configuration
│   │   │   ├── Cloudinary configuration
│   │   │   └── Mail configuration
│   │   │
│   │   ├── controllers/
│   │   │   ├── User controllers
│   │   │   ├── Profile controllers
│   │   │   ├── Course controllers
│   │   │   ├── Quiz controllers
│   │   │   ├── Payment controllers
│   │   │   ├── Admin controllers
│   │   │   ├── Student controllers
│   │   │   └── Certificate controllers
│   │   │
│   │   ├── middleware/
│   │   │   ├── Authentication
│   │   │   ├── Role-based authorization
│   │   │   ├── Rate limiting
│   │   │   └── Error handling
│   │   │
│   │   ├── models/
│   │   │   └── Mongoose schemas
│   │   │
│   │   ├── routes/
│   │   │   └── Express API routes
│   │   │
│   │   ├── services/
│   │   │   ├── AuthService
│   │   │   ├── StudentService
│   │   │   ├── QuizEvaluationService
│   │   │   ├── PdfQuizExtractorService
│   │   │   └── CertificatePdfService
│   │   │
│   │   ├── tests/
│   │   │   └── Jest unit and integration tests
│   │   │
│   │   ├── app.js
│   │   └── server.js
│   │
│   └── package.json
│
├── frontend/
│   ├── src/
│   │   ├── Components/
│   │   │   └── Reusable components and route guards
│   │   │
│   │   ├── Pages/
│   │   │   └── Student, Instructor, and Admin pages
│   │   │
│   │   ├── services/
│   │   │   └── Axios API client and endpoints
│   │   │
│   │   ├── slices/
│   │   │   └── Redux Toolkit slices
│   │   │
│   │   └── store/
│   │       └── Redux store configuration
│   │
│   └── package.json
│
├── docs/
│   ├── baseline-audit.md
│   ├── api-inventory.md
│   ├── database-model-audit.md
│   ├── architecture.md
│   ├── security.md
│   └── api.md
│
├── LICENSE
└── README.md
```

**Note:** This tree summarizes the structure supplied for the project. Consult the actual repository for the complete list of files and modules.

---

## ⚡ Quick Start

Follow the steps below to run the application locally.

### Prerequisites

Install:

* Node.js 18 or newer, subject to compatibility with the installed dependencies.
* npm.
* MongoDB Atlas or a compatible MongoDB deployment.
* Cloudinary credentials.
* Razorpay test credentials.
* Google Generative AI credentials if PDF quiz generation is enabled.
* SMTP credentials if email functionality is enabled.

The Node.js version used for production should be verified against the current deployment configuration.

### 1. Clone the Repository

```bash
git clone https://github.com/adarsh2027dev/Edtech-projects.git
cd Edtech-projects
```

### 2. Configure the Backend

Navigate to the backend:

```bash
cd backend
```

Install dependencies:

```bash
npm install
```

Create the environment configuration.

**Linux / macOS / Git Bash:**

```bash
cp .env.example .env
```

**Windows PowerShell:**

```powershell
Copy-Item .env.example .env
```

Configure the environment variables in `backend/.env`.

Then start the backend:

```bash
npm run dev
```

The backend is documented to run at:

```text
http://localhost:5000
```

Health check:

```text
http://localhost:5000/api/health
```

The actual port and health route depend on the current backend configuration.

### 3. Configure the Frontend

Open a second terminal:

```bash
cd frontend
```

Install dependencies:

```bash
npm install
```

Create the frontend environment file:

```bash
cp .env.example .env
```

On Windows PowerShell:

```powershell
Copy-Item .env.example .env
```

Configure the frontend API base URL according to the actual variable name in the Vite application.

Start the frontend:

```bash
npm run dev
```

The documented frontend development URL is:

```text
http://localhost:5173
```

### 4. Open the Application

Visit:

```text
http://localhost:5173
```

Confirm that the frontend can communicate with the backend and that the backend can connect to MongoDB.

---

## 🔑 Environment Variables

The frontend and backend maintain separate environment configurations.

The corresponding `.env.example` files should be treated as the authoritative references for exact variable names.

### Backend Configuration

Typical configuration categories include:

| Variable Category           | Purpose                                                     |
| --------------------------- | ----------------------------------------------------------- |
| Database URI                | Connect to MongoDB Atlas.                                   |
| JWT access secret           | Sign access tokens.                                         |
| JWT refresh secret          | Sign refresh tokens.                                        |
| Frontend URL                | Configure frontend integration and relevant CORS policies.  |
| Backend URL                 | Configure application URLs and integrations where required. |
| Cloudinary credentials      | Upload and deliver images.                                  |
| Razorpay credentials        | Create and verify payments.                                 |
| Google Generative AI key    | Enable AI-assisted PDF quiz generation.                     |
| SMTP credentials            | Enable email delivery.                                      |
| Cookie and session settings | Configure secure authentication behavior.                   |

These categories do not replace the exact variable names required by the source code.

### Frontend Configuration

Vite exposes environment variables prefixed with `VITE_` to client-side code.

Use frontend environment variables only for values that are safe to expose publicly, such as a public API base URL.

**Never place private API keys, JWT signing secrets, Razorpay secret keys, or database credentials in `VITE_` variables.**

### Environment Security

* Keep `.env` files out of version control.
* Use `.env.example` for documentation.
* Never commit real API credentials.
* Use separate development and production credentials.
* Rotate credentials if they are exposed.
* Validate required variables during startup.
* Restrict production database access.

---

## 🧪 Automated Testing

The project documents separate testing workflows for the backend and frontend.

### Backend Tests — Jest

Run:

```bash
cd backend
npm test
```

The supplied project documentation identifies tests for:

* Authentication.
* Role-based access control.
* Course creation.
* Unit-level business logic.
* Integration behavior.

Named examples include:

```text
rbac.test.js
createCourse.test.js
auth.test.js
```

The actual test coverage depends on the current repository implementation.

### Frontend Tests — Vitest

Run:

```bash
cd frontend
npm test
```

Use the configured Vitest test suite to validate frontend components and related application behavior.

### Recommended Test Coverage

| Area             | Suggested Test Scenarios                                              |
| ---------------- | --------------------------------------------------------------------- |
| Authentication   | Login, logout, token expiry, refresh, and invalid credentials.        |
| Sessions         | Multi-device sessions, revocation, and expired sessions.              |
| Authorization    | Student, Instructor, and Admin permission boundaries.                 |
| Courses          | Course creation, updates, and access control.                         |
| Quiz Generation  | Invalid PDFs, extraction errors, and malformed AI responses.          |
| Quiz Evaluation  | Correct answers, incorrect answers, and invalid submissions.          |
| Certificates     | Eligibility, PDF generation, and verification.                        |
| Payments         | Invalid signatures, duplicate requests, and payment state validation. |
| Learning Streaks | Consecutive days, missed days, and time-zone boundaries.              |
| Discussions      | Question creation, nested answers, and upvoting.                      |

These are recommended test scenarios and should not be interpreted as proof that each test already exists.

### Production Build Verification

Run the frontend and backend checks separately according to their package scripts.

Confirm that linting, tests, and production builds pass before deploying.

---

## 🛡️ Security Architecture

The application includes several layers of security.

### 1. Role-Based Access Control

The backend validates permissions for protected endpoints.

Role checks should be enforced at the API layer instead of relying exclusively on frontend route guards.

### 2. JWT Authentication

Access and refresh tokens have separate responsibilities.

* Access tokens authorize authenticated requests.
* Refresh tokens support session renewal.
* HTTP-only cookies help protect refresh tokens from direct JavaScript access.
* Multi-device session records support session tracking.

Refresh-token rotation, revocation, and replay protection should be verified against the implementation.

### 3. HTTP Security Headers

Helmet provides security-related HTTP headers.

The exact configuration should be reviewed for content security policy, framing restrictions, and other relevant protections.

### 4. NoSQL Injection Mitigation

The application uses `express-mongo-sanitize` to mitigate common NoSQL injection patterns.

This should be combined with input validation, safe query construction, and appropriate database permissions.

### 5. Rate Limiting

`express-rate-limit` helps limit excessive requests to configured endpoints.

Apply suitable limits to sensitive operations such as login, OTP verification, token refresh, and expensive AI-processing endpoints.

### 6. Payment Integrity

Razorpay signatures are verified server-side using HMAC SHA-256.

The server should validate payment data before updating payment-related records.

### 7. Secure File Handling

PDF uploads and other files should be validated for size, type, and processing limits.

Do not trust the original filename or client-provided MIME type alone.

### 8. Secrets Management

Keep credentials and private keys on the server.

Use environment variables or an appropriate secrets-management system for deployment configuration.

---

## 📈 Performance and Scalability

The current architecture provides several opportunities for improving performance as usage grows.

### Database Optimization

* Review query patterns and indexes.
* Optimize frequently used aggregation pipelines.
* Avoid unnecessary repeated database queries.
* Apply pagination to large collections.
* Monitor database query latency.

### API Optimization

* Validate requests early.
* Keep response payloads appropriately sized.
* Use consistent pagination and filtering.
* Apply rate limits to expensive operations.
* Avoid blocking the event loop with CPU-intensive tasks.

### AI Quiz Generation

PDF extraction and AI generation can be resource-intensive.

Recommended improvements include:

* PDF size limits.
* Processing timeouts.
* AI request limits.
* Structured error handling.
* Usage monitoring.
* Asynchronous processing for larger workloads when necessary.

### Frontend Optimization

* Split large routes into smaller bundles where appropriate.
* Lazy-load noncritical components.
* Optimize images and other assets.
* Avoid unnecessary React renders.
* Monitor bundle size and loading performance.

These improvements should be prioritized using measured performance data rather than assumptions.

---

## 🚀 Deployment

The deployment process should keep frontend and backend configuration consistent.

### Backend Deployment

Deploy the Express API to a Node.js-compatible hosting environment.

Configure:

* Production database URI.
* JWT secrets.
* Razorpay credentials.
* Cloudinary configuration.
* Google Generative AI credentials, if enabled.
* SMTP credentials, if enabled.
* Frontend origin and CORS settings.

Set the production port according to the hosting provider.

### Frontend Deployment

Build and deploy the Vite application using a compatible static hosting provider.

Configure the production API base URL using the correct Vite environment variable.

Ensure the backend accepts requests from the deployed frontend origin.

### Production Checklist

* [ ] Production environment variables configured.
* [ ] Database access restricted appropriately.
* [ ] CORS configured for trusted origins.
* [ ] Authentication and authorization verified.
* [ ] Payment verification tested.
* [ ] AI API limits configured.
* [ ] Upload limits configured.
* [ ] Tests passing.
* [ ] Production build successful.
* [ ] Error logging configured.
* [ ] Dependency vulnerabilities reviewed.

**Deployment note:** Confirm the current hosting providers and deployment configuration in the repository before assuming that either application is already deployed to a particular service.

---

## 📚 Project Documentation

The repository includes technical documentation to support development and maintenance.

| File                                                           | Description                                     |
| -------------------------------------------------------------- | ----------------------------------------------- |
| [`docs/baseline-audit.md`](docs/baseline-audit.md)             | Baseline architecture and implementation audit. |
| [`docs/api-inventory.md`](docs/api-inventory.md)               | API endpoint inventory.                         |
| [`docs/database-model-audit.md`](docs/database-model-audit.md) | Database schema and index audit.                |
| [`docs/architecture.md`](docs/architecture.md)                 | High-level system architecture.                 |
| [`docs/security.md`](docs/security.md)                         | Security architecture and controls.             |
| [`docs/api.md`](docs/api.md)                                   | API specifications and examples.                |

These documents provide additional context for developers working on the application.

---

## 🗺️ Future Enhancements

Potential future improvements include:

* Real-time learning progress updates.
* Enhanced instructor analytics.
* Expanded assessment and question-bank management.
* Advanced learning recommendations.
* Improved certificate administration.
* Additional accessibility improvements.
* More extensive integration testing.
* Expanded monitoring and operational dashboards.
* Improved AI-generated quiz review workflows.
* Automated deployment and security checks.

These are potential enhancements rather than claims about existing functionality.

---

## 🤝 Contributing

Contributions that improve functionality, security, reliability, accessibility, and documentation are welcome.

### Contribution Workflow

1. Fork the repository.
2. Create a feature branch.
3. Implement the change.
4. Add or update tests where appropriate.
5. Run the relevant test suites.
6. Verify the production build.
7. Update documentation.
8. Submit a pull request.

### Branch Naming Examples

```text
feature/ai-quiz-generation
feature/certificate-verification
feature/learning-analytics
fix/authentication-security
fix/payment-verification
docs/readme-improvements
```

### Contribution Guidelines

* Follow the existing project structure.
* Keep changes focused.
* Avoid committing secrets.
* Validate all incoming API data.
* Preserve role-based access restrictions.
* Test payment-related changes carefully.
* Document new environment variables.
* Include tests for critical business logic.

---

## 📜 License

This project is distributed under the **MIT License**, as indicated by the repository's supplied license information.

See the [`LICENSE`](LICENSE) file for the complete license terms.

---

## 👨‍💻 Developer and Project Links

**Project:** Kodemates EdTech — Full-Stack Learning Management System

**Repository:** [adarsh2027dev/Edtech-projects](https://github.com/adarsh2027dev/Edtech-projects)

**Development Team:** Team Kodemates

**Developer:** Adarsh Tiwari

**GitHub Profile:** [adarshtiwaridev](https://github.com/adarshtiwaridev)

---

## ⭐ Support the Project

If you find this project useful for learning or development, consider starring the repository and sharing your feedback.

Contributions, bug reports, and suggestions can help improve the platform.

---

## 🎓 Final Note

Kodemates EdTech combines a modern MERN architecture with secure authentication, role-based learning workflows, AI-assisted quiz generation, automated PDF certificates, Razorpay payment verification, learning streaks, analytics, and community discussions.

The project demonstrates how a full-stack application can bring together frontend development, backend architecture, database design, third-party integrations, and application security in a practical education platform.

**Kodemates EdTech — Building better digital learning experiences. 🚀**
