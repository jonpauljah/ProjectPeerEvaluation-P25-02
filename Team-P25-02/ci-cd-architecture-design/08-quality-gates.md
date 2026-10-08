<a id="section-8"></a>

# Quality Gates

| Quality Gate | Passing Criteria |
| --- | --- |
| Application build | Application build succeeds. |
| Code quality | Linting and formatting checks pass. |
| Automated testing | Required unit, integration, regression, and applicable end-to-end tests pass. |
| Dependency and security checks | Dependency and security checks complete and meet the team's agreed blocking criteria. |
| Pull request reviews | Required pull request reviews are complete. |
| Merge protection | A deliberately failing required check prevents merge. |
| Staging validation | After staging deployment, required health checks and smoke tests pass before the staged release is considered validated. |
