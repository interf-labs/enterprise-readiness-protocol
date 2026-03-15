# Agent Onboarding Protocol

An open standard for declaring what AI-powered solutions need from enterprise environments to deliver value.

Vendor teams declare an onboarding contract — plain English requirements with verifiable acceptance criteria. Enterprises self-prepare. No more mid-flight surprises.

## Install

```bash
npx skills add interf-labs/agent-onboarding-protocol
```

Or install specific skills:

```bash
npx skills add interf-labs/agent-onboarding-protocol --skill declare
npx skills add interf-labs/agent-onboarding-protocol --skill preview
```

Also available via the Interf CLI:

```bash
npx interf
```

## Skills

| Skill | Purpose |
|---|---|
| `declare` | Scan a codebase and declare an `interf.yaml` onboarding contract |
| `preview` | Preview enterprise rollout against company profiles (timelines, stakeholders, risks) |
| `protocol` | The protocol specification — schema, canonical dependency types, examples |

## The Contract: interf.yaml

Each requirement is a `what` + `ready` pair — what you need from enterprise, and how they know it's done:

```yaml
name: acme-crm-automation
version: 0.2.0
description: Automates CRM data entry and follow-up scheduling

requirements:
  - what: Read/write access to your CRM (contacts and opportunities)
    ready: We can create a contact and read an opportunity via API from our staging environment

  - what: SSO endpoint for our service to authenticate your users
    ready: A test user can log into our app via your SSO and see their CRM data

  - what: Someone from your data team to map your custom fields to our schema (~4 hours)
    ready: Field mapping document completed and signed off by both sides

  - what: Test environment with sample CRM data for validation
    ready: We can run our full test suite against the environment without errors

optional:
  - what: Webhook endpoint for real-time update notifications
    ready: We receive a test webhook payload within 5 seconds of a CRM update
```

## How It Works

1. **Declare** — Vendor teams use coding agents to scan their codebase and extract an `interf.yaml` contract. Or write it manually.
2. **Deliver** — Contract is sent to enterprise (via Interf platform, email, or however you work today).
3. **Resolve** — Enterprise works through each requirement. Each item has `ready` criteria so there's no ambiguity.
4. **Verify** — When all requirements are resolved, the solution is clear to deploy.

## Canonical Dependency Types

Dependencies can be anything in plain English. Optional canonical types enable deterministic matching across vendors and enterprises.

| Category | Covers |
|---|---|
| `integration.*` | CRM, ERP, HRIS, email, webhooks, ticketing, analytics |
| `auth.*` | SSO (SAML/OIDC), API credentials, service accounts |
| `data.*` | Historical exports, field mapping, sample data, PII |
| `infra.*` | Test environments, network/firewall, compute |
| `stakeholder.*` | Data team, security, IT admin, executive sponsor |
| `process.*` | Security review, legal/DPA, procurement, training |

See [skills/protocol/types/](./skills/protocol/types/) for the full type reference with match patterns.

## Repository Structure

```
skills/
├── declare/SKILL.md                          ← Declare onboarding contract
├── preview/SKILL.md                          ← Preview enterprise rollout
└── protocol/
    ├── SKILL.md                              ← Protocol overview (routing index)
    ├── spec.md                               ← interf.yaml schema specification
    ├── examples.md                           ← Example contracts
    └── types/                                ← Canonical dependency types (3-layer)
        ├── index.md                          ← L0: Quick-scan category index
        ├── integration/overview.md           ← L1: Integration types overview
        ├── integration/crm.md                ← L2: CRM type details
        └── ...                               ← (18 detail files across 6 categories)
```

## Contributing

The canonical dependency types grow over time. To propose a new type:

1. Add entries to the appropriate `types/<category>/<detail>.md` file
2. Update the `types/<category>/overview.md` table
3. Update `types/index.md` quick match table if applicable
4. Submit a PR with a description of what use-case the new type covers

## License

MIT — [Interf, Inc.](https://interf.com)
