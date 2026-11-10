# Hosting and deployment

Choose hosting together with the client. A workflow that runs on a personal laptop may stop when the laptop sleeps; a hosted service requires ongoing ownership, access control, monitoring, and cost management.

## Choose an operating model

- **Client-owned hosting (preferred):** Deploy into an account or project owned by the client. Ask them to grant you scoped access and identify who will maintain it.
- **Local or scheduled execution:** Suitable for a prototype or low-risk workflow where the client accepts availability limits. Protect the machine and credentials, and document who restarts it.
- **Managed automation platform or cloud service:** Check supported triggers, execution limits, secret handling, data locations, logs, costs, and cancellation behavior against the client's needs. Do not assume a platform is appropriate based on its name.

Before selecting a provider, confirm the expected availability, budget, data handling, region, account ownership, and support needs. Make sure the client understands recurring costs and service limits.

## Deployment checklist

- [ ] Confirm scope, owner, approval contact, supported hours, expected volume, and budget.
- [ ] Use a separate private repository, deployment, credentials, and data stores for this client.
- [ ] Document inputs, outputs, connected systems, required scopes, and data retention.
- [ ] Keep production secrets in managed secret storage; never commit them.
- [ ] Test with synthetic data, then use a client-approved test environment before production.
- [ ] Handle timeouts, retries, duplicate events, rate limits, and partial failures safely.
- [ ] Add a manual approval or dry-run mode for high-impact changes.
- [ ] Verify logs do not expose secrets or unnecessary personal/business data.
- [ ] Configure appropriate alerts and identify who responds when the workflow fails.
- [ ] Document how to pause, roll back, restore, and revoke access.
- [ ] Review costs, permissions, and retention after launch and at handover.

## Handover

Give the client a plain-language description of what the automation does, where it runs, which accounts it uses, how to pause it, how failures are reported, expected costs, and who supports it. Ensure the client can operate the system without your personal account or credentials.
