<a id="section-16"></a>

# CI Test Execution Plan

| Execution Point | Planned Validation |
| --- | --- |
| Commit / pull request | Build validation, lint/format checks, unit tests, integration tests, and agreed fast regression tests. |
| Pull request before merge | All required automated checks and quality gates must pass. |
| Main after merge | Full required CI validation and retained test/security evidence. |
| Staging deployment | Health checks, smoke tests, and selected critical workflow validation. |
| Milestone / final evidence | Results showing passed/failed tests, related defects, and traceability to requirements. |
