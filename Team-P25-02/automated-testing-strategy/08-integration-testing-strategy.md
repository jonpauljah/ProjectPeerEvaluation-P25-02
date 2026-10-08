<a id="section-8"></a>

# Integration Testing Strategy

| Area | Requirement |
| --- | --- |
| Backend and database | Validate backend routes against a controlled MongoDB test environment. |
| Authorization | Verify protected routes with valid, invalid, missing, and insufficient authorization. |
| Data relationships | Verify course, roster, team, rubric, evaluation, response, and reporting data relationships. |
| CSV upload | Verify CSV upload behavior from request through persisted result. |
| Email integration | Verify email behavior through a controlled sandbox/test configuration rather than real student recipients. |
| Test setup and cleanup | Use repeatable setup/teardown or seeded data so tests do not depend on prior runs. |
| Failure diagnosis | Produce clear failures that identify the component boundary that failed. |
