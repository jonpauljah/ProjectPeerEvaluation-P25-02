<a id="section-4"></a>

## 3. Non-Functional Requirements

| ID | Quality Attribute | Requirement |
| --- | --- | --- |
| NFR-01 | Maintainability | New CI/CD code, tests, configuration, and documentation shall use clear organization, consistent naming, and documented responsibilities. |
| NFR-02 | Repeatability | The same source version and configuration shall produce a consistent build and test result in supported environments. |
| NFR-03 | Reliability | Failed required checks or failed deployment validation shall stop the applicable workflow and report the failure. |
| NFR-04 | Security | Credentials, tokens, connection strings, and environment values shall not be committed to the repository and shall use approved secret storage. |
| NFR-05 | Privacy | Automated and staging tests shall use synthetic, de-identified, or sponsor-approved data and shall not email real students unintentionally. |
| NFR-06 | Traceability | Requirements, tests, defects, pull requests, pipeline results, and milestone evidence shall be traceable through the repository and project documentation. |
| NFR-07 | Portability | The documented containerized environment shall run consistently on supported developer systems and CI runners. |
| NFR-08 | Configurability | Environment-specific URLs, credentials, and service settings shall be supplied through configuration rather than hard-coded production values. |
| NFR-09 | Usability | Setup, pipeline, deployment, and troubleshooting documentation shall be understandable to a future maintainer with relevant software-development skills. |
| NFR-10 | Recoverability | Deployment and release documentation shall identify how to return to the last known working version when supported by the selected platform. |
| NFR-11 | Functional Preservation | Existing PEERS functionality shall be preserved whenever practical, and changes introduced by the project shall not cause validated workflows to regress. |

<br>
