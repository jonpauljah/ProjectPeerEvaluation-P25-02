<a id="section-5"></a>

## Validation Plan

The container stack must prove that it can start and operate as one system. The project specification, Containerization requirement, explicitly asks for service health checks and startup documentation. Docker health checks should test MongoDB readiness and a backend health endpoint when one exists, while smoke checks should confirm that the frontend can reach the API. These checks create evidence that the containers are working as one system.

| Check | Expected result | Evidence to retain |
| --- | --- | --- |
| Build images | Frontend and backend images build from a clean checkout. | Build output and image tags. |
| Start Compose stack | All defined services remain running and healthy. | Compose status output and health status. |
| Database connection | Backend connects to MongoDB and completes a safe startup action. | Backend log line without secrets. |
| Email sandbox | A test invitation is captured by the local or staging test inbox. | Message view or test result with no student data. |
| Core smoke path | A user can load the application and reach a safe API endpoint. | Automated smoke test result. |
| Clean setup repeat | A second supported machine follows the guide without undocumented steps. | Reviewer checklist and issue record. |
