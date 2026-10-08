<a id="section-4"></a>

# Target CI/CD Architecture

The target architecture is a GitHub-based workflow where developers work on feature branches, open pull requests into main, and GitHub Actions automatically validates each proposed change. Only changes that satisfy the required checks and reviews should be merged. After an approved merge, the exact validated version should deploy automatically to staging, where health checks and smoke tests confirm that the release is usable.

| Stage | Target Behavior |
| --- | --- |
| Feature branch | Developer makes an isolated change without working directly on main. |
| Pull request | Change is reviewed before merge. The current team proposal uses two reviewer approvals. |
| CI validation | GitHub Actions runs build, lint/format checks, automated tests, dependency checks, and security checks. |
| Quality gate | Required failed checks prevent the pull request from merging. |
| Merge to main | Only approved, validated changes become part of the shared baseline. |
| Staging deployment | The approved merged version deploys automatically to the staging environment. |
| Staging validation | Health checks and smoke tests verify frontend/backend availability, database connectivity, and selected workflows. |
| Production | Production deployment automation is outside the current capstone scope and remains subject to sponsor approval. |
