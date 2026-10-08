<a id="section-2"></a>

## Current Findings

The documented container setup does not match the inherited application. The architecture review identifies that the prior Docker Compose file refers to PostgreSQL even though PEERS uses MongoDB through Mongoose. A PostgreSQL service cannot prove that the PEERS backend connects to its expected database, so the configuration must be replaced or removed. This finding establishes the main correction for the container plan.

| Finding | Effect on PEERS | Required response |
| --- | --- | --- |
| Compose database does not match MongoDB | Local setup can fail or use a false database dependency. | Define a MongoDB service and use the backend connection variable. |
| Environment values are partly hard coded | Local and staging behavior can diverge. | Move host names, ports, secrets, and email settings to environment configuration. |
| Email can contact an external SMTP provider | Test activity can send messages outside the project. | Use Mailtrap for local environment and in staging environments. |
| Service readiness is not proven | The frontend or backend can start before dependencies are ready. | Add health checks and dependency conditions where supported. |
| Setup steps depend on developer knowledge | New developers can reach different results. | Provide one startup command and a short validation checklist. |
