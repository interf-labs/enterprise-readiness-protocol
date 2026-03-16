---
id: integration.ticketing.api
name: Ticketing & Project Management
category: integration
systems: [jira, servicenow, zendesk, freshdesk, linear, asana]
requires: [auth.api-credentials]
blocked_by: [process.security-review]
related: [integration.webhook.outbound, stakeholder.it-admin]
sectors: [all]
---

# Ticketing & Project Management

Vendor needs to read or write tickets in the enterprise support or project management system. Common for customer support automation, incident management, and workflow tools.

## Template

- **what:** API access to your ticketing system for reading and creating tickets
- **ready:** Our service can read a test ticket, add an internal note, and update its status

## Matches

Use this type when vendor says: "access to your ticketing system", "Jira/ServiceNow/Zendesk integration", "create/update tickets", "support queue access", "issue tracker"
