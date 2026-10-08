<a id="section-18"></a>

# 6. Modernization Workflows

Modernization workflows are separated from PEERS functional workflows because they are new engineering processes introduced by this capstone rather than inherited professor or student business behavior. They are nevertheless required project workflows because they provide the automated controls used to preserve and validate the application.

| ID | Modernization Workflow | Primary Actor | Required Outcome | Related Requirement |
| --- | --- | --- | --- | --- |
| MW-01 | Repeatable Environment Setup | Developer / Maintainer | Documented setup and container configuration initialize the frontend, backend, MongoDB connection, and required supporting services in a repeatable manner. | FR-11, FR-12 |
| MW-02 | Automated CI Validation | Developer / GitHub Actions | A pushed commit or pull request triggers dependency installation, build, lint/format checks, automated tests, dependency validation, and security scanning. | FR-13 through FR-18 |
| MW-03 | Pull Request Quality Gate and Merge Control | Developer / Reviewers / GitHub | Changes targeting main cannot be merged until the required validation checks pass, and the applicable branch-protection requirements are satisfied. | FR-19, FR-20 |
| MW-04 | Automated Staging Deployment | GitHub Actions / Staging Platform | A successful approved change is deployed automatically to the separate staging environment. | FR-21 |
| MW-05 | Post-Deployment Validation | CI/CD Pipeline | After staging deployment, health checks and selected smoke validation confirm application availability, database connectivity, and selected critical workflow usability. | FR-22 |
| MW-06 | Pipeline and Deployment Evidence | CI/CD Pipeline / Maintainer | Logs or reports retain evidence of build, test, dependency/security, and deployment results for review and demonstration. | FR-23 |

<br>
