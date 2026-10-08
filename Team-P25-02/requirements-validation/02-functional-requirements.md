<a id="section-3"></a>

## 2. Functional Requirements

| ID | Type | Requirement |
| --- | --- | --- |
| FR-01 | Authentication | The system shall allow an authorized professor to authenticate and access professor functions. |
| FR-02 | Course Management | The system shall allow a professor to create and manage courses. |
| FR-03 | Roster Management | The system shall allow a professor to upload and process a student roster from a CSV file. |
| FR-04 | Team Management | The system shall allow students to be organized into course teams. |
| FR-05 | Evaluation Management | The system shall allow a professor to create and distribute a peer-evaluation activity. |
| FR-06 | Evaluation Management | The system shall generate individualized evaluation access links or tokens for eligible students. |
| FR-07 | Evaluation Management | The system shall support evaluation invitations and reminders through the configured email service. |
| FR-08 | Evaluation Management | The system shall allow a student to submit a peer evaluation through the assigned link. |
| FR-09 | Data Management | The system shall store course, roster, team, evaluation, and response data in MongoDB. |
| FR-10 | Report Management | The system shall allow a professor to review and export supported evaluation results and reports. |
| FR-11 | Development Environment | The project shall provide documented, repeatable setup procedures for the frontend, backend, database connection, and required external services. |
| FR-12 | Development Environment | The project shall provide Dockerfiles and Docker Compose configuration that reflect the application's MongoDB architecture. |
| FR-13 | Continuous Integration | Each code commit pushed to the repository and each pull request targeting main shall automatically trigger the required CI workflow. |
| FR-14 | Continuous Integration | The CI workflow shall build the application and run configured linting and formatting checks. |
| FR-15 | Continuous Integration | The CI workflow shall run automated unit and integration tests. |
| FR-16 | Continuous Integration | The project shall use Jest and React Testing Library for appropriate frontend automated tests. |
| FR-17 | Continuous Integration | The project shall use Playwright for agreed end-to-end and regression workflows. |
| FR-18 | Continuous Integration | The CI workflow shall perform dependency and security checks and make the results available to maintainers. |
| FR-19 | Continuous Integration | Required failed checks shall prevent a pull request from being merged into main. |
| FR-20 | Continuous Integration | The main branch shall be protected so that application changes are merged through pull requests and required validation checks must pass before merging. |
| FR-21 | Continuous Delivery | A successful approved change shall automatically deploy to the staging environment after required checks pass. |
| FR-22 | Continuous Delivery | After each staging deployment, the pipeline shall execute health checks and the selected smoke tests to validate application availability, database connectivity, and critical workflows. |
| FR-23 | Continuous Delivery | The project shall retain logs or reports sufficient to demonstrate pipeline, test, security, and deployment results. |
| FR-24 | Continuous Integration / Continuous Delivery | The project shall automate deployment to a staging environment only. Production hosting, production deployment, and production-release automation shall remain outside the project's scope. |
| FR-25 | Documentation | The project shall document setup, configuration, testing, pipeline behavior, deployment, rollback, release, and troubleshooting procedures. |

<br>
