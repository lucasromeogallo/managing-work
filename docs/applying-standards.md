# Applying these standards to a company project

Use this repository as the shared reference for separate company-specific applications and automations. It does not contain those applications, and it should not become a shared home for company code, configuration, credentials, or data.

## Starting a project

1. Create a separate private repository and deployment/runtime for the company or client. Prefer ownership by the company or client, with only the access needed for the work.
2. Review the [shared standards index](README.md) and select the documents relevant to the project. The project brief and suggested layout are starting points; they are not a required technology stack.
3. Copy and adapt only the materials the project needs. If the company repository can reliably access this core repository, it may link to the relevant guidance instead; otherwise include an appropriate reviewed copy.
4. Record the source repository and revision/date of any copied guidance in the company repository, and review it when the shared source changes. Keep one authoritative copy of each policy within that company's project.
5. Fill in the [project brief](../templates/automation-project/PROJECT_BRIEF.md) using non-sensitive descriptions. Do not put client records, secrets, or confidential examples in the shared repository.
6. Confirm the company's requirements, approvals, ownership, data flows, operating model, and handover needs before connecting production systems or handling sensitive data.

## Adapting the baseline

The shared documents describe practical defaults, not universal legal or compliance requirements. For each project:

- Confirm which guidance applies and who approves the choices.
- Add company-specific requirements only in that company's repository, with the appropriate owner and review process.
- Document material decisions, tradeoffs, and exceptions with the [decision record template](../templates/automation-project/DECISION_RECORD.md).
- Keep credentials, business data, company-specific configuration, and production logs out of this core repository.
- Do not assume a vendor, hosting service, framework, or AI provider is selected or approved by these standards.

For details, use the [privacy and separation guidance](client-separation-and-privacy.md), [hosting checklist](hosting-and-deployment.md), and [integration guidance](integrations.md). Pause and confirm requirements with the company or client when data sensitivity, applicable rules, ownership, or approval is unclear.
