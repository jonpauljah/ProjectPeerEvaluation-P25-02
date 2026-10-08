# External Dependencies

[Back to assessment overview](README.md)

## 7. External Dependencies

### 7.1 Current State

The inherited system relies on external packages and services for frontend build operations, linting, authentication, email, file processing, database access, and deployment. Several packages are declared, but no active use was identified in the Technical Overview, indicating that dependency cleanup should be considered as part of maintainability work.

| Dependency / Group | Role or Finding | Status |
| --- | --- | --- |
| react-scripts | Frontend development server, build process, and test commands. | Active |
| concurrently / cross-env | Local development startup and environment handling. | Active |
| @babel/core | JavaScript transformation for the React build. | Active |
| ESLint + React plugins | Static code-quality checking. | Active |
| uuid | Used by tooling/database setup; not declared as a direct active-application dependency. | Tooling / review |
| Render | Referenced by deployment documentation as the intended hosting approach; current live deployment was not independently verified. | Documented staging deployment dependency |
| Charting/form/upload/date libraries | Several packages such as chart.js/recharts, formik/yup, react-dropzone, and date-fns are declared but no active usage was identified. | Unused |
| Testing-library packages | Declared in the frontend but no implemented automated frontend tests were found. | Present, unused |

### 7.2 Planned Direction

Frontend development and production build tooling will migrate from Create React App/react-scripts to Vite while retaining React. The existing react-scripts dependency remains part of the current baseline until the migration is complete.

Dependency management should be simplified by removing or justifying unused declarations, ensuring both frontend and backend installations are reproducible from lockfiles, and adding automated dependency/security checking as part of the CI process. The specific scanning configuration will be defined in the CI/CD Architecture Design.

## Related Documents

- [Dependency Risks](../dependency-risks.md)
