# Shared project standards

This repository is the shared standards and starter-materials home for small-business automation projects. Use it as the cross-project reference when creating a separate repository for a company or client; keep each company's application, configuration, and data in its own repository.

> **This is a standards repository, not a finished automation product or a company application.** It currently also contains a GitHub Issues and Projects workshop lab under `.github/`. No client-specific automation, hosting, or Muse/Claude integration is implemented here.

## Start here

1. Review the [shared standards index](docs/README.md) to find the guidance relevant to your work.
2. Follow [the guide for applying these standards](docs/applying-standards.md) when creating a company-specific repository.
3. Use [the project brief](templates/automation-project/PROJECT_BRIEF.md) and [suggested project structure](templates/automation-project/README.md) as starting points, adapting them to the project rather than treating them as application code.
4. Before handling client information or deploying, review [client separation and privacy](docs/client-separation-and-privacy.md) and [hosting and deployment](docs/hosting-and-deployment.md).
5. Add external AI or other services only after review, behind the boundaries described in [integration guidance](docs/integrations.md).

## A safe default for each client

- Create a **separate private repository and deployment** for each client. Do not put different clients' credentials, data, or automation runs in one shared project.
- Prefer a repository and cloud/service accounts owned by the client, with access granted to you only as needed. Agree on ownership, access, costs, support, and handover before deployment.
- Use synthetic or anonymized data while learning and testing. Never commit passwords, API keys, access tokens, personal data, customer exports, or production logs.
- Start with a small, reversible workflow and a manual approval step before enabling actions that send messages, change records, or spend money.
- Treat AI-generated code and outputs as untrusted drafts. Review, test, and validate them before use; do not let generated code run directly in production.

These are practical safeguards, not legal, security, or compliance advice. Confirm the client's requirements and applicable rules before handling regulated or sensitive information.

## Repository map

- [`docs/README.md`](docs/README.md) — index of shared guidance and repository-level references.
- [`docs/applying-standards.md`](docs/applying-standards.md) — how to use this core repository as the baseline for separate company projects.
- `docs/` — privacy, hosting, and integration guidance; each document's scope and source are listed in the index.
- `templates/automation-project/` — copyable project brief, suggested layout, and decision-record template.
- `.github/` — existing GitHub Issues and Projects workshop lab assets; they are not client automation examples.
- [`CONTRIBUTING.md`](CONTRIBUTING.md), [`SECURITY.md`](SECURITY.md), [`SUPPORT.md`](SUPPORT.md), and [`CODE_OF_CONTENT.md`](CODE_OF_CONTENT.md) — guidance for this repository and its contributors.

## Contributing and support

See [CONTRIBUTING.md](CONTRIBUTING.md) for local workflow and review guidance and [SUPPORT.md](SUPPORT.md) for help with this repository. Do not open a public issue or pull request containing a secret, client name, personal information, or other confidential details. See [SECURITY.md](SECURITY.md) for private reporting guidance.

## License

This repository is licensed under the MIT License; see [LICENSE](LICENSE). Before copying material into a client project, confirm that the license and any third-party terms meet your and the client's needs.
