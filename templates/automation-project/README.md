# Automation project starter

Use this folder as a reference when starting a **separate private repository for one client**. Follow [the core repository's project guidance](../../docs/applying-standards.md), then copy only the brief and templates needed and adapt them. This starter documents a suggested structure; it does not contain application code or select a hosting or AI vendor.

## Suggested structure

```text
client-automation/
  README.md                 # Purpose, setup, operation, and ownership
  .gitignore
  .env.example              # Placeholder names only; never credentials
  docs/
    workflow.md             # Trigger, steps, inputs, outputs, failure paths
    runbook.md              # Monitor, pause, recover, and hand over
    decisions/              # Important choices and tradeoffs
      decision-record.md    # Copy from this template for each major decision
  src/
    workflows/              # Business rules and orchestration
    integrations/
      providers/             # AI/model adapters, if approved and needed
      systems/               # Email, CRM, accounting, or other adapters
  tests/                     # Synthetic test data and automated checks
```

Start with only the files needed. Add a language, framework, or dependency only when the project requires it. Never place client secrets or data in this shared template repository.

For significant choices, copy [`DECISION_RECORD.md`](DECISION_RECORD.md) to `docs/decisions/decision-record.md` in the company's repository, then update its metadata and sections. Keep company-specific decision records there.

## Before production

Complete the [deployment checklist](../../docs/hosting-and-deployment.md) and [client separation and privacy guidance](../../docs/client-separation-and-privacy.md). Confirm the client owns or approves the repository, hosting account, credentials, data flow, monitoring, and handover plan.
