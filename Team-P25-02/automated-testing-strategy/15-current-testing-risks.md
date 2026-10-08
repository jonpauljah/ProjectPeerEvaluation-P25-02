<a id="section-17"></a>

# Current Testing Risks

| Risk | Impact | Planned Response |
| --- | --- | --- |
| No established backend automated test framework | Critical backend behavior cannot be reliably gated in CI. | Add framework/scripts and start with high-risk backend logic and routes. |
| Frontend testing infrastructure exists but suite maturity is unconfirmed | The team may overestimate current test coverage. | Inventory existing test files and run the current test command to establish the baseline. |
| Manual test\_api.js may be mistaken for automated coverage | A diagnostic script can pass without providing broad or repeatable validation. | Treat it as a diagnostic artifact and implement structured tests with assertions and CI-compatible exit status. |
| Expected behavior is unclear for some inherited features | Tests could automate the wrong behavior. | Confirm acceptance criteria with the sponsor before locking regression expectations. |
| Legacy code may be difficult to isolate | Unit testing may require refactoring. | Refactor carefully only where needed for maintainability/testability while preserving validated behavior. |
| Email testing could reach real users | Privacy and communication risk. | Use an approved email sandbox and synthetic recipients. |
| Environment inconsistency | Tests may pass locally and fail in CI/staging. | Correct Docker/database configuration and use documented environment-specific configuration. |
