# Planned Development Environment

[Back to validation overview](README.md)

## 5. Planned Development Environment

The planned PEERS development environment will use Docker Compose to provide a repeatable local setup for Windows, macOS, and Linux. Docker Compose will run the React frontend, Express backend, and MongoDB database. Mailtrap will be used as an external email-testing service for both local development and staging, with separate sandboxes for each environment.

Native npm commands will remain available as an alternative to Docker Compose. These improvements will reduce manual configuration and establish a consistent environment for development and automated testing.

### 5.1 Environment Architecture and Local Setup

The planned development environment will include the following components:

| Component | Implementation | Purpose |
| --- | --- | --- |
| Frontend | React Docker container | Runs the PEERS user interface locally. |
| Backend | Express Docker container | Runs the API and handles JWT authentication. |
| Database | MongoDB Docker container | Stores development data. |
| Email | Email Sandbox | Captures outgoing test emails. |
| Docker Compose | Container orchestration | Coordinates the three containers and passes the required configuration to them. |

## Related Documents

- [Containerization Assessment](../containerization-assessment.md)
