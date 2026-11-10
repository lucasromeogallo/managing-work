# Integration boundaries

This repository does not include an integration with Muse, Claude, or any other AI provider. “Muse” is not specific enough here to identify a product or API, so no vendor capabilities, SDKs, or behavior are assumed. Verify the exact product and its official documentation before planning an implementation.

## Keep providers replaceable

For a client project, keep workflow/domain logic separate from external services. Use a small adapter boundary for each provider or integration, for example:

```text
src/
  workflows/       # Business rules and orchestration
  integrations/
    providers/     # AI/model provider adapters
    systems/       # Client-approved business system adapters
```

Define each adapter by the inputs it accepts, the output shape it returns, errors it can produce, and the data it is allowed to receive. Normalize provider responses before passing them to the workflow. Keep provider-specific SDK types and configuration inside the adapter so the workflow does not depend on one vendor.

## If using an AI provider

- Verify product identity, supported API, current terms, data retention, training use, region, and client approval from official sources.
- Send only the minimum necessary information; remove or mask identifiers when possible.
- Keep API keys in managed secrets, never in source code or prompts.
- Treat provider output as untrusted input. Validate its format, constrain allowed actions, and require review for consequential operations.
- Do not execute generated code or generated tool instructions directly. Use deterministic validation and explicit allowlists for any downstream action.
- Set sensible timeouts, limits, and cost controls, and handle provider errors without silently continuing with invalid or partial output.

An adapter boundary makes a later Muse or Claude integration possible, but it does not imply compatibility or security. Select and implement a provider only after confirming the client's requirements and the provider's current documentation.
