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

- [CI/CD Architecture Design](../ci-cd-architecture-design.md)
