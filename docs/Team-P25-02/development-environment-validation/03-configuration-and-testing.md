<a id="04-planned-configuration-and-services"></a>

# Planned Configuration and Supporting Services

[Back to validation overview](README.md)

### 5.2 Environment Configuration and Secret Management

The team will provide a complete .env.example file documenting the required MongoDB, JWT, SMTP, application URL, and server settings. Developers will supply their own values through untracked local .env files.

Hard-coded API addresses and the inherited JWT secret fallback will be addressed to support secure, environment-specific configuration. Local development, CI, and staging will use separate credentials and configuration.

Mailtrap credentials for local development will be stored in developers' untracked environment files. GitHub Actions Secrets will protect CI credentials, while Render will manage staging secrets, including the separate staging Mailtrap credentials.

Further details on CI/CD configuration and environment separation will be documented in the CI/CD Architecture Design.

### 5.3 Database and Email Testing

The development environment will use a dedicated MongoDB container with synthetic test data. Documented seeding and reset procedures will allow developers to initialize the database and reproduce consistent testing conditions.

Mailtrap will provide email testing for both local development and staging, using separate sandboxes to keep their messages isolated. The local backend will connect to the development Mailtrap sandbox through SMTP, allowing developers to inspect evaluation invitations, reminders, and other supported emails without contacting real students.

Unlike MongoDB, Mailtrap will not run as a Docker container. It is a hosted service that requires network access. Detailed staging configuration and email validation will be covered in the CI/CD Architecture Design and Automated Testing Strategy.

## Related Documents

- [CI/CD Architecture Design](../ci-cd-architecture-design/README.md)

<a id="05-testing-and-validation-criteria"></a>

# Planned Testing Support and Validation Criteria

[Back to validation overview](README.md)

### 5.4 Automated Testing Support

The planned development environment will support local unit and integration testing using isolated configuration and controlled test data. Developers will be able to run these tests before submitting changes, while GitHub Actions will execute the required automated test suite.

Tests involving the database will use reproducible seeding and reset procedures. Email tests will use mocks or an appropriate Mailtrap sandbox when actual SMTP integration needs to be verified.

The Automated Testing Strategy will define testing frameworks, test cases, fixtures, regression and end-to-end coverage, and execution requirements. This document will focus on ensuring that the local development environment supports those testing activities.

### 5.5 Validation Criteria for Implementation

After implementing the planned improvements, the team will validate the completed development environment against the following criteria.

| Validation Area | Expected Result |
| --- | --- |
| Setup and execution | A developer can clone the repository and start the frontend, backend, and MongoDB through Docker Compose. |
| Application connectivity | The frontend communicates with the intended local backend, which successfully connects to MongoDB. |
| Email functionality | The local backend sends test emails to the development Mailtrap sandbox without contacting real recipients. |
| JWT authentication | Protected functions work with valid JWTs using the configured signing secret. |
| Environment configuration | Required settings are documented and supplied without committing secrets. |
| Automated testing | Unit and integration tests run locally using controlled test data and reproducible database seeding and reset procedures. |

The team will record validation results using relevant screenshots, terminal output, and other supporting evidence.

## Related Documents

- [Automated Testing Strategy](../automated-testing-strategy/README.md)
