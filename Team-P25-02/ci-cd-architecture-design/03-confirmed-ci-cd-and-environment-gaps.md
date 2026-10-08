<a id="section-3"></a>

# Confirmed CI/CD and Environment Gaps

| Current Finding | Why It Matters | Required Direction |
| --- | --- | --- |
| docker-compose.yml provisions PostgreSQL and sets a PostgreSQL DATABASE\_URL. | The backend application actually uses MongoDB/Mongoose, so the current Compose file does not represent the real database architecture. | Replace the PostgreSQL service/configuration with the approved MongoDB-based local/test architecture and validate the full stack. |
| No GitHub Actions workflow files were identified. | Build, testing, dependency/security validation, merge gates, and staging deployment are not automated. | Create GitHub Actions workflows during Milestones 2 and 3 based on the Milestone 1 architecture. |
| Backend package.json has no test script/framework. | Backend logic cannot currently participate in a repeatable CI test gate. | Add an agreed backend automated test framework and scripts. |
| A manual backend test\_api.js script exists. | It calls one local API endpoint with Axios and logs output, but it is not a repeatable automated unit/integration suite. | Replace or supplement diagnostic scripts with structured automated tests that produce reliable pass/fail results. |
| A real .env file is tracked under src/backend. | Committed environment values may expose secrets or cause inconsistent environment behavior. | Use .env.example for documented placeholders and approved secret stores for protected values. |
| The backend already provides GET /api/health. | A health endpoint gives the delivery pipeline an existing way to verify service availability after deployment. | Use or extend the endpoint as part of staging health validation. |
