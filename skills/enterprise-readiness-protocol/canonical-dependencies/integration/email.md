---
id: integration.email.api
name: Email System Integration
category: integration
systems: [microsoft-365, exchange, google-workspace, gmail]
requires: [auth.api-credentials]
blocked_by: [process.security-review]
related: [integration.messaging.api, auth.sso.oidc]
sectors: [all]
---

# Email System Integration

Vendor needs to read or send email through the enterprise email system. Common for automation solutions that send notifications, follow-ups, or process email-based workflows.

## Template

- **what:** Access to your email system for sending and reading messages on behalf of users
- **ready:** Our service can send a test email on behalf of a test user through your email system

## Matches

Use this type when vendor says: "send emails on behalf of users", "access to your email platform", "email integration", "Gmail/Outlook/Exchange access", "email automation"
