---
id: auth.service-account
name: Service Account
category: auth
systems: []
requires: [stakeholder.it-admin]
blocked_by: [process.security-review]
related: [auth.api-credentials]
sectors: [all]
---

# Service Account

Dedicated service identity (not tied to a human user) for vendor's automated processes. Unlike personal API credentials, a service account ensures that integrations continue to work regardless of employee turnover and can be scoped to least-privilege permissions.

## Template

- **what:** Service account with appropriate permissions for our automated workflows
- **ready:** Our service can authenticate as the service account and perform all required operations

## Matches

Use this type when vendor says: "service account", "machine identity", "non-human account", "bot account", "dedicated service identity", "automated process credentials"
