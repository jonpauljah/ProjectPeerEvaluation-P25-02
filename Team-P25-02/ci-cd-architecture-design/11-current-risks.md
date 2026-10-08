<a id="section-11"></a>

# Current Risks

| Risk | Impact | Planned Response |
| --- | --- | --- |
| Docker configuration does not match MongoDB architecture | Local/CI/staging environments may not reproduce the actual application. | Replace PostgreSQL references and validate the MongoDB-based service layout. |
| No CI workflow exists yet | Changes can be merged without automated build/test/security validation. | Implement the Milestone 1 design as GitHub Actions in Milestone 2. |
| Backend automated testing is not established | CI cannot reliably validate backend behavior. | Add test framework/scripts and prioritize critical backend workflows. |
| Tracked .env file / configuration issues | Potential secret exposure and environment inconsistency. | Review, remove sensitive values, rotate if required, and use secret stores. |
| Legacy defects block automation | Tests or deployments may fail for inherited reasons. | Classify findings using the agreed defect boundary and fix material blockers. |
| Proposed staging services are not fully confirmed | Milestone 3 delivery implementation could be delayed. | Resolve platform/access decisions before Milestone 3 implementation. |
