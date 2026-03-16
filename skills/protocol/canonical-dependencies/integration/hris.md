---
id: integration.hris.api
name: HRIS Access
category: integration
systems: [workday, successfactors, bamboohr, adp, namely, rippling]
requires: [auth.api-credentials, stakeholder.it-admin]
blocked_by: [process.security-review, process.compliance-review]
related: [data.field-mapping, stakeholder.business-owner]
sectors: [all]
---

# HRIS Access

Vendor needs access to the enterprise HR information system for employee profiles, organizational structure, or workforce data. Common for tools that provision users, sync org charts, or automate HR workflows.

## Template

- **what:** Read access to your HRIS (employee profiles and org structure)
- **ready:** We can query the employee directory and retrieve org chart data via API

## Matches

Use this type when vendor says: "HRIS integration", "employee data", "org chart access", "Workday/BambooHR integration", "HR system access", "people data"
