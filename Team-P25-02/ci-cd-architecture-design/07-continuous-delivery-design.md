<a id="section-7"></a>

# Continuous Delivery Design

Continuous Delivery begins after a change has passed CI and has been approved for merge. The automated delivery target for this project is staging only.

| Area | Requirement |
| --- | --- |
| Deployment source | Use the exact merged commit that passed the required validation as the deployment source. |
| Staging deployment | Deploy the frontend and backend to the approved staging environment. |
| Configuration and secrets | Supply staging-specific configuration and protected values through environment configuration/secret storage. |
| Database connection | Connect the backend to the staging MongoDB environment. |
| Health validation | Use the existing /api/health endpoint, plus any additional checks needed, to verify backend availability. |
| Smoke testing | Run the selected smoke tests after deployment. |
| Failure handling | Fail the applicable workflow when deployment, health validation, or required smoke testing fails. |
| Deployment evidence | Retain deployment and validation evidence for milestone review and final handoff. |
