# Deployment and Containerization

[Back to assessment overview](README.md)

## 9. Deployment Procedures

### 9.1 Current State

The repository contains manual deployment documentation centered on Render. The documented model deploys the React frontend as a Render static site and the Node.js/Express backend as a Render web service, with external MongoDB and SMTP services configured through environment variables. The SLA records no confirmed live production site for the inherited baseline.

| Finding | Assessment |
| --- | --- |
| Manual procedure | Deployment steps are documented, but a repository-managed automated deployment workflow is not established. |
| Frontend build-path mismatch | Existing documentation refers to src/frontend as the build location even though the frontend package configuration and active build run from the repository root. |
| Missing documented variable | JWT_SECRET is required by the backend but is missing from the primary deployment guide. |
| Dashboard-managed infrastructure | No checked-in Render infrastructure configuration was identified, so manually configured hosting settings cannot be verified from source control. |
| Alternative platforms | Vercel, Railway, and Docker/cloud hosting are discussed as possibilities but are not established as implemented deployment environments. |

### 9.2 Planned Direction

The project will automate deployment to a separate staging environment after required validation succeeds. The staging approach will useRender for the frontend and backend, MongoDB Atlas for the database, and Mailtrap  for email capture. Production hosting, production deployment, and production-release automation are outside the agreed scope. Detailed deployment workflow behavior belongs in the CI/CD Architecture Design.

## 10. Containerization Status

### 10.1 Current State

Containerization is not currently operational. The repository contains a docker-compose.yml file and sample Docker-related documentation, but the Compose configuration does not accurately represent the implemented application.

| Finding | Assessment |
| --- | --- |
| Database mismatch | Docker Compose provisions PostgreSQL even though PEERS uses MongoDB through Mongoose. |
| Missing Dockerfiles | Compose references frontend and backend build contexts without corresponding implemented Dockerfiles. |
| Configuration mismatch | Compose uses configuration names that do not match the environment variables read by the application. |
| Documentation-only example | A sample Dockerfile appears in deployment documentation, but this is not an implemented container build in the repository. |

### 10.2 Planned Direction

The team will complete a MongoDB-aligned containerized environment and validate that the frontend, backend, database connection, environment configuration, and required supporting services operate reliably. Detailed Dockerfile, Compose, service-health, and startup decisions will be defined in the separate Containerization Assessment.

## Related Documents

- [Current Deployment Procedures and Gaps](../current-deployment-procedures-and-gaps.md)
- [Containerization Assessment](../containerization-assessment.md)
- [CI/CD Architecture Design](../ci-cd-architecture-design.md)
