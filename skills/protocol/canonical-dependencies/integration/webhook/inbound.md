---
id: integration.webhook.inbound
name: Inbound Webhook
category: integration
systems: []
requires: [stakeholder.it-admin]
blocked_by: [process.security-review, process.architecture-review]
related: [integration.webhook.outbound, infrastructure.network-access]
sectors: [all]
---

# Inbound Webhook

Enterprise needs to expose an HTTP endpoint that the vendor calls to deliver events or data. The enterprise is the receiver — the vendor pushes data to the enterprise's system when events occur.

## Template

- **what:** An HTTPS endpoint on your side to receive event notifications from our service
- **ready:** Enterprise endpoint receives and acknowledges a test webhook payload from our service

## Matches

Use this type when vendor says: "we'll send you events", "you expose an endpoint", "push notifications to your system", "callback URL", "we call your API"
