# Security and privacy

This repository is a learning and starter space; it is not a security or compliance certification. Before building or hosting a workflow for a business, agree on what data it handles, who can access it, where it runs, and how it can be stopped and recovered.

## Handling client information

- Keep client work in a separate private repository and deployment per client. Do not copy one client's records, credentials, or configuration into another client's project.
- Do not commit credentials, personal information, customer records, exports, private logs, or confidential business details. Use synthetic data for examples, tests, and screenshots.
- Store required credentials only in the hosting platform's secret manager or another approved secrets manager. Give each integration its own limited-purpose credential and rotate or revoke it when access is no longer needed.
- Send a third-party or AI provider only the minimum information needed for the task, after confirming the client allows it. Check the provider's current privacy, retention, and data-processing terms rather than assuming data is not retained.
- Avoid logging request bodies, tokens, personal data, and generated content unless necessary and explicitly approved. Establish appropriate retention and access limits for logs and backups.
- Do not deploy generated code or enable irreversible actions without review, tests, and a rollback or manual recovery plan.

## Reporting a vulnerability or exposure

Please do not publish secrets, client information, or actionable vulnerability details in a public issue or pull request. Use GitHub's private vulnerability reporting feature for this repository if it is enabled. Otherwise, contact the repository owner privately through an account channel they have provided. Do not include live credentials or customer data in a report; redact them and revoke/rotate exposed credentials immediately.

For an accidental exposure, first remove access to the exposed credential or data, then notify the affected client and repository owner through an appropriate private channel. Deleting a secret from the latest commit does not erase it from Git history, clones, logs, or caches; rotate it and follow the hosting provider's guidance for cleanup.
