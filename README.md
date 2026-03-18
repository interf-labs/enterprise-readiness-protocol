# Enterprise Readiness Protocol

An open standard for defining and verifying readiness for enterprise rollouts.

## Install

```bash
npx skills add interf-labs/enterprise-readiness-protocol
```

Then tell your coding agent:

```
draft a readiness contract for this project and preview rollout for BlackRock
```

## Skills

| Skill | Purpose |
|---|---|
| `interf-draft` | Draft a readiness contract (`interf.yaml`) |
| `interf-preview` | Preview enterprise rollout — timelines, stakeholders, risks |
| `enterprise-readiness-protocol` | Protocol specification (loaded automatically) |

## The Readiness Contract

```yaml
name: crm-automation
version: 0.2.0
description: Automates CRM data entry and follow-up scheduling

requirements:
  - what: Read/write access to your CRM (contacts and opportunities)
    ready: We can create a contact and read an opportunity via API from staging

  - what: SSO endpoint for our service to authenticate your users
    ready: A test user can log into our app via your SSO and see their data

  - what: Security review and approval for our integration
    ready: Security review completed and vendor approved

optional:
  - what: Webhook endpoint for real-time update notifications
    ready: We receive a test webhook payload within 5 seconds of a CRM update
```

## How It Works

1. **Draft** — Vendor drafts `interf.yaml` — the readiness contract declaring every requirement.
2. **Deliver** — Contract is published to the Interf registry or sent directly to enterprise.
3. **Resolve** — Enterprise works through each requirement, audited against the `ready` criteria.
4. **Verify** — All requirements resolved. Rollout can proceed.

## Related

| Repo | Purpose |
|---|---|
| [interf-labs/cli](https://github.com/interf-labs/cli) | CLI tooling — validate, publish, preview |
| [interf.com](https://interf.com) | Documentation |

## License

MIT — [Interf, Inc.](https://interf.com)
