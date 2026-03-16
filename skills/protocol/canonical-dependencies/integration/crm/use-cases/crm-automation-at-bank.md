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

Security review was the critical path — required SOC2 Type II report and penetration test results before any API access was granted. Custom object permissions required involvement from a Salesforce admin shared across departments — scheduling was the bottleneck. Field mapping needed 2 rounds because the first mapping missed picklist value translations.

## Critical Path

1. Security review (blocks everything)
2. CRM API credentials (after security clears)
3. Field mapping (parallel, needs data team)
4. SSO setup (parallel, straightforward)

## Key Takeaway

Start security review on day 1 — it's the critical path at banks. Everything else can run in parallel once security clears.
