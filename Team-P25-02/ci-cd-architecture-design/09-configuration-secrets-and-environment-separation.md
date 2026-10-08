<a id="section-9"></a>

# Configuration, Secrets, and Environment Separation

| Area | Requirement |
| --- | --- |
| Tracked source files | Remove real secrets and environment-specific credentials from tracked source files. |
| Configuration example | Keep a safe .env.example or equivalent documentation showing required variable names without real values. |
| Secret storage | Store protected values in GitHub/hosting-platform secret stores. |
| Environment separation | Use separate local, staging, and any future production configuration, credentials, data, and email behavior. |
| Environment-specific settings | Move environment-specific URLs and service settings out of hard-coded application logic when required for repeatable deployment. |
| Configuration documentation | Document the minimum configuration needed to build, test, run, and deploy the system. |
