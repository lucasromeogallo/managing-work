# Client separation and privacy

Small-business automations may connect systems that contain sensitive information. Keep boundaries clear from the first experiment; a private repository alone does not isolate a running service or its credentials.

## One client, one project boundary

For each client, create a separate private repository and a separate deployment/runtime. Use separate credentials, environment variables, storage, logs, backups, and service accounts. Do not create a shared folder or deployment that mixes clients. If an exception is genuinely required, agree on the design and isolation controls with the client before implementation.

Prefer accounts, cloud projects, and hosting that the client owns. Have the client grant you only the access needed for the work, and agree who pays, operates, monitors, and supports the automation. Remove your access and revoke credentials at handover or when work ends.

## Minimize data

1. Write down what the automation needs to read and change. Ask for the smallest required fields and permissions.
2. Prototype with invented or anonymized data. Do not use a real customer export just because it is convenient.
3. Before connecting production systems, confirm the client has authority to share the data and approve the selected services and data flows.
4. Define where data passes, where it is stored, who can see it, how long it is kept, and how it is deleted. Include logs, backups, test fixtures, and AI-provider requests.
5. Use synthetic data in tests and examples. Redact sensitive details from screenshots, issue reports, commit history, and support messages.

## Credentials and access

- Keep secrets out of source, prompts, documentation, terminal transcripts, issues, and logs.
- Use a local untracked `.env` file only for development when appropriate; commit a placeholder-only `.env.example`, never a real `.env`.
- In production, use the hosting platform's managed secret storage. Do not bake credentials into code, images, or deployment files.
- Use distinct, limited-scope credentials per integration and environment. Rotate them if exposed and revoke them when no longer needed.
- Require multi-factor authentication where available, review collaborators regularly, and grant the smallest necessary permissions.

## Safe operations

Start with read-only access or a dry run. Test failure cases, duplicate events, retries, and rate limits. Require a human confirmation for high-impact actions such as sending external messages, changing financial or customer records, or initiating payments. Provide a way to pause the workflow and a documented recovery path.

Do not treat this checklist as legal or compliance advice. For regulated or sensitive data, pause until the client has confirmed the applicable requirements and approved the architecture and vendors.
