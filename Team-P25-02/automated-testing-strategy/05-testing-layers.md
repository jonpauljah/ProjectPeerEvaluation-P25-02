<a id="section-5"></a>

# Testing Layers

| Test Level | Purpose | PEERS Examples |
| --- | --- | --- |
| Unit | Validate isolated business logic quickly. | Authentication/authorization logic, token logic, CSV validation, rubric validation, calculations, eligibility logic. |
| Integration | Validate interaction between application components/services. | Express routes + MongoDB, auth + protected routes, roster persistence, evaluations/responses, reporting, controlled email service. |
| Functional Regression | Protect agreed workflows from breaking after changes. | Login, course creation, roster upload, team assignment, rubrics, evaluation distribution, student submission, reporting. |
| End-to-End | Validate representative user workflows across the running application. | Instructor and student browser journeys using Playwright. |
| Smoke | Verify that the staged release is alive and usable after deployment. | Frontend/backend reachability, MongoDB connectivity, /api/health, and a selected critical workflow. |
