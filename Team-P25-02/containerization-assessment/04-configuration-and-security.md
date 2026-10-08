<a id="section-4"></a>

## Configuration and Security

Local and staging environments need different values without exposing secrets. The architecture review identifies hard-coded settings and credential handling as high-priority concerns. A committed .env.example file should name every required variable without real values, while .env and staging secrets remain outside version control. This boundary keeps the Compose file readable and prepares the project for CI secret storage.

| Configuration area | Local approach | Staging approach |
| --- | --- | --- |
| Database connection | Use the Compose service host, port, and a development database name. | Use the approved MongoDB Atlas connection string from protected secrets. |
| JWT and token secrets | Load placeholder-free values from an ignored local .env file. | Load protected values from the deployment platform or GitHub Actions secrets. |
| Email delivery | Route SMTP to Mailtrap so messages stay in the local test inbox. | Route SMTP to Mailtrap. |
| Frontend API URL | Use the local backend route defined for the Compose network or browser proxy. | Use the deployed staging API address. |
| Logs and debug mode | Use readable console logs without student data. | Use deployment logs with debugging limited to approved settings. |
