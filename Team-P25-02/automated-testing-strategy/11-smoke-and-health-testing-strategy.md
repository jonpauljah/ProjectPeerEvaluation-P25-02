<a id="section-13"></a>

# Smoke and Health Testing Strategy

| Area | Requirement |
| --- | --- |
| Frontend availability | Verify that the staging frontend is reachable. |
| Backend availability | Verify that the staging backend is reachable. |
| Health endpoint | Call the existing GET /api/health endpoint and confirm a successful health response. |
| Database connectivity | Verify that the backend can connect to the staging MongoDB database. |
| Critical workflow | Verify a small selected critical workflow after deployment. |
| Email safety | Verify that staging email is captured by the approved sandbox and does not reach unintended real users. |
| Validation enforcement | Fail deployment validation when required health/smoke checks do not pass. |
