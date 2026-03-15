---
id: integration.crm.api
use_case: CRM automation at a Fortune 500 bank
sector: financial-services
system: salesforce
dependencies_triggered:
  - integration.crm.api
  - auth.sso.saml
  - process.security-review
  - process.compliance-review
  - stakeholder.data-team
  - data.field-mapping
---

# CRM Automation at a Fortune 500 Bank

Vendor deployed CRM data entry automation at a major US bank using Salesforce Enterprise.

## What Happened

Security review took 5 weeks (vs typical 2 weeks). Required SOC2 Type II report and penetration test results. Custom object permissions required involvement from Salesforce admin shared across 3 departments — scheduling was the bottleneck. Field mapping needed 2 rounds because first mapping missed picklist value translations.

## Dependencies

| Dependency | Resolution Time | Blocker? |
|---|---|---|
| Security review | 5 weeks | Yes — blocked all API access |
| SSO (SAML via Okta) | 1 week | No |
| CRM API credentials | 3 days (after security cleared) | No |
| Data team for field mapping | 2 weeks (2 sessions) | No |
| Compliance review (PII) | 2 weeks (parallel with security) | No |

## Key Takeaway

Start security review on day 1 — it's the critical path at banks. Everything else can run in parallel once security clears.
