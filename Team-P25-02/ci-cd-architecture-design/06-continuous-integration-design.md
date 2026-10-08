<a id="section-6"></a>

# Continuous Integration Design

Continuous Integration will validate proposed changes before they are merged into main. The pipeline should turn the current manual build/test process into a repeatable automated quality gate.

| Area | Requirement |
| --- | --- |
| Workflow triggers | Trigger the required CI workflow for each code commit pushed to the repository and each pull request targeting main, consistent with the approved requirements. |
| Dependency installation | Install dependencies using the repository lock files and fail the workflow if dependency installation fails. |
| Application build | Build the React application using the existing npm build command. |
| Code quality | Run ESLint/formatting validation using the agreed project rules. |
| Automated testing | Run the automated test suites defined in the Automated Testing Strategy. |
| Dependency and security checks | Run dependency and security checks and expose results to maintainers. |
| Merge requirements | Require configured checks to pass before merge. |
| Branch protection | Protect main so normal changes are merged through pull requests rather than direct unvalidated changes. |
| Logs and reports | Retain logs/reports needed to demonstrate pipeline, test, security, and build results. |
