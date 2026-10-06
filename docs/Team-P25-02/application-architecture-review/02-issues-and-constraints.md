# Architecture Issues and Constraints

[Back to architecture review overview](README.md)

## Architecture Review

The inherited PEERS architecture provides a relatively simple three-tier structure and clear separation between the frontend, backend, and database. However, the architecture review identified several issues and constraints that may affect maintainability, reliability, portability, security, and future deployment. The following table summarizes the primary architectural concerns, their potential impact, and their relative priority for the current modernization effort. Detailed implementation plans for containerization, automated testing, and CI/CD are documented in their respective Milestone 1 deliverables.

| Architecture issue | Business impact | Priority | Notes |
| --- | --- | --- | --- |
| Docker configuration does not match the application's database architecture | The existing Docker Compose configuration references PostgreSQL even though PEERS uses MongoDB. This prevents the documented container environment from accurately representing the application and can make setup unreliable for developers. | HIGH | Update the container architecture to use MongoDB and match the actual React, Node.js/Express, and MongoDB application structure. Detailed remediation should be covered in the Containerization Assessment. |
| Complete repeatable container architecture is missing | Developers cannot reliably reproduce the same frontend, backend, and database environments, increasing setup effort and the chance of environment-specific problems. | HIGH | Frontend, backend, MongoDB, configuration, and required supporting services need a documented and repeatable container structure. |
| Environment-specific configuration is partially hard-coded | Hard-coded URLs or environment settings can cause the application to behave differently between local and staging environments and make deployment more difficult to maintain. | HIGH | Environment-dependent settings should be supplied through external configuration rather than embedded directly in application code. |
| Secret and credential handling requires improvement | Improperly stored credentials, tokens, or connection values can expose sensitive configuration and make secure environment separation difficult. | HIGH | Secrets should be removed from committed configuration and supplied through approved environment or secret-storage mechanisms. |
| Backend functionality runs within a single application process | A failure or heavy workload in one backend responsibility can affect the entire PEERS backend because authentication, courses, evaluations, reporting, and other modules share the same Node.js process and database connection. | MEDIUM | The modular monolith remains appropriate for the current project size. The goal is to preserve module boundaries rather than introduce microservices. |
| Email operations occur synchronously during API requests | Email delivery can increase request-processing time and an external SMTP delay or failure can affect the user-facing request being processed. | MEDIUM | The current architecture does not use a background worker or message queue for email operations. This should be documented as a limitation rather than necessarily redesigned within the current project scope. |
| CSV imports rely on temporary local server storage | Local temporary storage can complicate portability and horizontal scaling because uploaded files are tied to the individual backend instance processing the request. | MEDIUM | This is acceptable for the current scale but should be documented as a constraint for future scaling or multi-instance deployment. |
| Backend modules may become increasingly coupled as the application grows | Shared models and application state can make future changes harder to isolate and maintain, increasing the chance that modifications to one area affect another. | MEDIUM | Preserve clear module boundaries between authentication, courses, rosters, teams, evaluations, reporting, and professor settings. |
| Automated validation is limited in the inherited architecture | Changes to application components can introduce regressions without being detected early, reducing confidence that existing professor and student workflows remain functional. | HIGH | This review should identify the architectural concern only. The detailed solution belongs in the Automated Testing Strategy and CI/CD Architecture Design |

## Related Documents

- [Containerization Assessment](../containerization-assessment.md)
- [Automated Testing Strategy](../automated-testing-strategy.md)
- [CI/CD Architecture Design](../ci-cd-architecture-design.md)
