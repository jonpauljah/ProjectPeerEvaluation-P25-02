<a id="section-15"></a>

# Test Data, Privacy, and Email Safety

| Area | Requirement |
| --- | --- |
| Test data selection | Use synthetic, de-identified, or sponsor-approved test data. |
| Student information | Do not place real student information in automated test fixtures unless explicitly approved and required. |
| Database isolation | Use isolated test/staging databases rather than production personal data. |
| Email safety | Use safe recipients or a staging email sandbox. |
| Reproducibility | Reset or seed data so repeated runs are reproducible. |
| Secret storage | Keep database credentials, SMTP credentials, tokens, and other environment secrets outside the repository. |
| Configuration review | Review the currently tracked backend .env file and remediate any real secrets or environment-specific values. |
