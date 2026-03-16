---
id: integration.messaging.api
name: Messaging Platform Integration
category: integration
systems: [slack, microsoft-teams, google-chat]
requires: [auth.api-credentials, stakeholder.it-admin]
blocked_by: [process.security-review]
related: [integration.email.api, integration.webhook.outbound]
sectors: [all]
---

# Messaging Platform Integration

Vendor needs to post messages or interact with the enterprise messaging platform. Common for solutions that provide notifications, alerts, or interactive workflows via chat.

## Template

- **what:** Access to your messaging platform for posting notifications and alerts
- **ready:** Our service can post a test message to a designated test channel

## Matches

Use this type when vendor says: "Slack integration", "Teams notifications", "send messages to your channels", "chat platform access", "post to Slack", "bot in Teams"
