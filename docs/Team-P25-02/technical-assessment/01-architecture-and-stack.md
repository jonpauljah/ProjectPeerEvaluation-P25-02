# Architecture and Stack

[Back to assessment overview](README.md)

## 3. Software Architecture Summary

The current PEERS application uses a three-tier web architecture. A React single-page frontend communicates with a Node.js/Express REST API, and the backend uses Mongoose to access MongoDB. Email operations are performed through Nodemailer and an external SMTP provider. The backend is implemented as a modular monolith, with authentication, courses, rosters, teams, evaluations, reporting, and professor settings separated by responsibility but deployed as one application.

This structure is appropriate for the current project size and is not planned for replacement. The primary technical objective is to strengthen the delivery, configuration, testing, and staging infrastructure around the inherited application. Detailed current-state and target-state diagrams, architecture issues, quality attributes, and architecture goals are maintained in the separate Application Architecture Review.

## 4. Technology Stack

### 4.1 Current Technology Stack

| Area | Current Technology | Current Role |
| --- | --- | --- |
| Frontend | JavaScript, HTML, CSS, React, Material UI (MUI), React Router DOM, Axios | Provides the browser UI, navigation, reusable interface components, and REST API communication. |
| Backend | Node.js, Express.js 4 | Defines REST API endpoints and server-side application logic. |
| File processing | Multer, csv-parser | Handles CSV roster upload and parsing. |
| Database | MongoDB, Mongoose 8 | Provides persistent application storage, schemas, validation, and database queries. |
| Authentication | bcryptjs, jsonwebtoken | Hashes professor passwords and supports JWT-based professor API authentication. |
| Communication | Nodemailer, external SMTP provider | Sends evaluation invitations, reminders, and password-reset email. |
| Configuration | dotenv | Loads environment-dependent backend configuration. |
| Code quality/build support | ESLint, React tooling, Babel/react-scripts | Supports linting, frontend build operations, and JavaScript transformation. |

### 4.2 Planned Supporting Technologies

The core application stack will be preserved. The following technologies are identified in the SLA and project specification as the proposed supporting stack for testing, CI/CD, containerization, staging, and quality automation. Exact configuration and implementation details are documented in the corresponding Milestone 1 design and strategy documents.

| Technology | Planned Role |
| --- | --- |
| Jest / React Testing Library | Unit, integration, and frontend behavior testing. |
| Playwright | End-to-end and regression workflow validation. |
| ESLint / Prettier | Automated code-quality and formatting checks. |
| GitHub Actions | CI/CD orchestration and automated validation. |
| Docker / Docker Compose | Repeatable local and test environments. |
| Render | Proposed staging hosting for the React frontend and Node.js/Express backend. |
| MongoDB Atlas | Proposed managed staging database. |
| Mailtrap | Staging email sandbox that captures test messages without contacting real students |
| Dependabot / OWASP Dependency Check | Proposed dependency and security scanning support; detailed configuration remains part of CI/CD planning. |

## Related Documents

- [Application Architecture Review](../application-architecture-review.md)
