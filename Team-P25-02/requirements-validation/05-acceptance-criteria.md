<a id="section-6"></a>

## 5. Acceptance Criteria

| ID | Validation Area | Criterion |
| --- | --- | --- |
| AC-01 | Development Environment | A new maintainer can clone the team repository, supply documented configuration, and start the supported containerized environment. |
| AC-02 | Continuous Integration | Each code commit pushed to the repository and each pull request targeting main automatically triggers the required CI workflow, including build, linting, formatting, automated testing, dependency, and security checks. |
| AC-03 | Quality Gates | A deliberately failing required check prevents the pull request from being merged. |
| AC-04 | Automated Testing | Automated unit, integration, regression, and Playwright end-to-end tests collectively cover the confirmed priority workflows. |
| AC-05 | Continuous Delivery | A successful approved change to main automatically deploys the expected version to staging. |
| AC-06 | Continuous Delivery | The staging frontend and backend are reachable, the backend connects to the staging database, and required health checks pass. |
| AC-07 | Automated Testing | Smoke tests confirm that the selected critical workflow is usable after staging deployment. |
| AC-08 | Privacy | Staging email tests are captured by the approved sandbox and do not contact unintended real users. |
| AC-09 | Presentation and Demonstration | Pipeline, test, security, and deployment evidence are available for the final demonstration. |
| AC-10 | Documentation | Setup, configuration, testing, deployment, release, troubleshooting, known defects, deferred features, risks, and future-maintenance recommendations are documented and reviewed before final handoff. |

<br>
