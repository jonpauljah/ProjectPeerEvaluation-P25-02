# Stakeholders and Software Quality Attributes

[Back to architecture review overview](README.md)

## Stakeholders

| Name | Role |
| --- | --- |
| Dr. Geetika Vyas | Project Sponsor |
| Team P25-02 | Development and Modernization Team |
| University Faculty / Course Instructors | Primary System Users |
| Students | Primary System Users |
| Future Software Developers/Maintainers | Secondary System Users |
| Prof. Yan Huang | Capstone Professor |

## Software Quality Attributes

| Software Quality Attribute | Definition | Key success metrics | Notes |
| --- | --- | --- | --- |
| Maintainability | The application, CI/CD configuration, tests, and documentation should remain clearly organized and understandable so future developers can modify and maintain the system. | Clear module responsibilities; consistent configuration and naming; documented setup and maintenance procedures. | Further addressed in the Technical Assessment Report and final technical documentation. |
| Repeatability | The same source version and configuration should produce consistent build and test results across supported environments. | Builds and automated tests execute consistently; development and staging environments can be reproduced from documented configuration. | Further addressed in the Development Environment Validation, Containerization Assessment, and CI/CD Architecture Design. |
| Reliability | Failures in required validation or deployment checks should be detected, reported, and prevented from progressing through the delivery process. | Failed required checks stop the applicable workflow; failed staging validation is reported; health and smoke tests confirm successful deployment. | Further addressed in the CI/CD Architecture Design and Automated Testing Strategy. |
| Security | Credentials, tokens, connection strings, and other sensitive values should be protected and excluded from committed source code. | No sensitive values committed to the repository; approved secret-storage mechanisms are used; dependency and security checks run automatically. | Further addressed in the Technical Assessment Report and CI/CD Architecture Design. |
| Privacy | Development, testing, and staging environments should avoid exposing real student information or unintentionally contacting real users. | Tests use synthetic, de-identified, or sponsor-approved data; staging email behavior does not contact unintended users. | Further addressed in the Automated Testing Strategy and staging configuration documentation. |
| Traceability | Requirements, tests, defects, code changes, pipeline results, and milestone evidence should be traceable throughout the project. | Validated requirements can be linked to tests and supporting evidence; relevant project artifacts can be traced through documentation and repository history. | Further addressed in the Requirements Traceability Matrix. |
| Portability | The application should operate consistently across supported developer systems, CI runners, and the staging environment. | Containerized services run consistently across supported environments; machine-specific setup is minimized. | Further addressed in the Development Environment Validation and Containerization Assessment. |
| Configurability | Environment-specific values should be supplied through configuration rather than being hard-coded in application source code. | URLs, credentials, connection information, and service settings are externally configurable for local and staging environments. | Further addressed in the Technical Assessment Report and Containerization Assessment. |
| Usability | Setup, testing, deployment, and troubleshooting procedures should be understandable to future developers with appropriate technical experience. | Documentation provides clear procedures for setup, testing, deployment, and troubleshooting without requiring undocumented knowledge. | Further addressed in the final Technical Documentation, including setup, configuration, testing, deployment, release, and troubleshooting procedures. |
| Functional Preservation | Architectural and delivery-process changes should preserve validated PEERS functionality. | Existing critical workflows continue to pass regression and end-to-end testing after project changes. | Further addressed in the Requirements Validation, Critical Workflow Identification, and Automated Testing Strategy. |

## Related Documents

- [Requirements Traceability Matrix](../requirements-traceability-matrix.md)
