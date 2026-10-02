# Security and financial-risk notes

This repository contains agent-facing financial signal and copy-trading workflows, account and token routes, a backend cash/position ledger, research exports, and API descriptions. Treat account identifiers, bearer tokens, wallet references, positions, provider messages, and research exports as sensitive.

## Scope and limits

- The inspected backend source records signals and updates internal account/position state. No broker SDK or external brokerage order adapter was established by the reviewed repository tree. This does not prove how a separately deployed service behaves.
- User guides, agent skills, OpenAPI files, and hosted links may describe remote behavior. Their presence does not prove production availability, execution destination, permission scope, or real-money safety.
- Do not use real funds or long-lived broker credentials based on these repository examples. Verify service ownership, account authorization, order destination, loss limits, stop controls, idempotency, audit records, and recovery with the accountable operator first.
- Research schemas and export scripts do not prove anonymization. Inspect each generated export before sharing.
- No root `LICENSE` file was present in the inspected repository tree; reuse terms are unspecified.

## Reporting

Report vulnerabilities privately to the repository owner or through GitHub Security Advisories. Do not include tokens, account details, private user data, or exploitable production details in public issues.
