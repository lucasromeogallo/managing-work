# Contributing

Thanks for helping improve this learning and automation starter repository. Keep changes focused, beginner-friendly, and consistent with the guidance in the README.

## Before you contribute

- Never add real client identifiers, business records, credentials, exports, or production logs. Use fictional examples and synthetic data.
- Do not add a vendor SDK, API call, or claim about Muse or another provider without verified documentation and a clearly scoped need. Keep provider-specific behavior behind an adapter as described in [integration guidance](docs/integrations.md).
- Keep client-specific code and configuration in a separate private repository, not in this shared starter.

## Local checks

This repository is primarily Markdown plus a GitHub Issues and Projects workshop lab. There is no application build or automated test suite configured. Before submitting a change:

1. Preview edited Markdown and check its relative links.
2. If editing the workshop scripts or workflows, review the complete diff and test only in a repository you own that contains no client data. The issue-seeding script can delete repository issues when run with `--delete` or `--seed-all`; do not run it against a real client repository.
3. Check `git diff --check` for whitespace errors.

## Submitting changes

Use a focused branch and pull request. Describe what changed, how you checked it, and any limitations. Never include a secret or confidential client information in a commit, issue, pull request, screenshot, or log.
