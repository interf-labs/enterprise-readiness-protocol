---
id: integration.crm.bulk-export
name: Bulk CRM Data Export
category: integration
systems: [salesforce, hubspot, dynamics-365, zoho-crm]
requires: [auth.api-credentials, stakeholder.data-team]
blocked_by: [process.security-review, process.compliance-review]
related: [integration.crm.api, data.field-mapping]
sectors: [all]
---

# Bulk CRM Data Export

Vendor needs to perform bulk data exports from the enterprise CRM — full contact lists, account histories, deal pipelines, or activity logs. Distinct from real-time API access because it involves large-volume batch operations that may require elevated permissions and rate limit considerations.

## Template

- **what:** Bulk export access to your CRM data (contacts, accounts, and activity history)
- **ready:** We can initiate a bulk export job and retrieve a complete dataset from your CRM

## Matches

Use this type when vendor says: "bulk export", "full data dump", "export all contacts", "CRM migration", "historical CRM data", "batch extract from Salesforce"
