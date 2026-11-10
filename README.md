# Small-business automation projects

A practical home for learning, designing, and delivering small-business process automations. Use the project brief and guidance here to keep client work understandable, separated, and maintainable as you grow your coding skills.

> **This repository is a starter and learning space, not a finished automation product.** It currently contains a GitHub Issues and Projects workshop lab under `.github/`. No client-specific automation, hosting, or Muse/Claude integration is implemented here. Keep real client work in a separate private repository for each client.

## Start here

1. Read [the project brief template](templates/automation-project/PROJECT_BRIEF.md) and make a copy for a new project. Fill it in with non-sensitive details only.
2. Read [client separation and privacy](docs/client-separation-and-privacy.md) before collecting or handling client information.
3. Use [the suggested project structure](templates/automation-project/README.md) to start each automation in its own private repository.
4. Choose a hosting approach with the client using [the hosting and deployment checklist](docs/hosting-and-deployment.md).
5. Add external AI or other services only behind the provider boundaries described in [integration guidance](docs/integrations.md).

## A safe default for each client

- Create a **separate private repository and deployment** for each client. Do not put different clients' credentials, data, or automation runs in one shared project.
- Prefer a repository and cloud/service accounts owned by the client, with access granted to you only as needed. Agree on ownership, access, costs, support, and handover before deployment.
- Use synthetic or anonymized data while learning and testing. Never commit passwords, API keys, access tokens, personal data, customer exports, or production logs.
- Start with a small, reversible workflow and a manual approval step before enabling actions that send messages, change records, or spend money.
- Treat AI-generated code and outputs as untrusted drafts. Review, test, and validate them before use; do not let generated code run directly in production.

These are practical safeguards, not legal, security, or compliance advice. Confirm the client's requirements and applicable rules before handling regulated or sensitive information.

## Repository map

- `templates/automation-project/` — copyable brief and suggested layout for a client project.
- `docs/` — privacy, hosting, and integration guidance.
- `.github/` — existing GitHub Issues and Projects workshop lab assets; they are not client automation examples.
- `CONTRIBUTING.md` — safe development and contribution guidance.
- `SECURITY.md` — how to report security issues or accidental exposure.

## Contributing and support

See [CONTRIBUTING.md](CONTRIBUTING.md) for local workflow and review guidance and [SUPPORT.md](SUPPORT.md) for help with this repository. Do not open a public issue or pull request containing a secret, client name, personal information, or other confidential details. See [SECURITY.md](SECURITY.md) for private reporting guidance.

## License

This repository is licensed under the MIT License; see [LICENSE](LICENSE). Before copying material into a client project, confirm that the license and any third-party terms meet your and the client's needs.
