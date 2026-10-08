<a id="section-10"></a>

# Milestone 1 Decisions and Open Questions

| Decision / Question | Current Direction | Milestone 1 Action |
| --- | --- | --- |
| Priority workflows | Use the SLA workflow list as the initial regression/E2E scope. | Confirm final priority list with sponsor. |
| Pull request approval rule | Two reviewer approvals are currently proposed. | Confirm and configure branch protection later. |
| Staging host | Render is proposed and the repository already contains Render-related configuration notes. | Confirm access, service layout, and cost constraints. |
| Staging database | MongoDB Atlas is proposed and aligns with the actual MongoDB application architecture. | Confirm database ownership, access, and test-data approach. |
| Email sandbox | Mailtrap or approved equivalent is proposed. | Confirm acceptable tool and credentials. |
| Dependency/security scanner | Dependabot and/or OWASP tooling is proposed. | Select the exact tools and define blocking severity rules. |
| Production | Production hosting/release automation is outside the current project scope. | Keep staging and production scope clearly separated. |
