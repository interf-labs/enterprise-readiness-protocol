---
id: integration.webhook.outbound
name: Outbound Webhook
category: integration
systems: []
requires: [stakeholder.it-admin]
blocked_by: [process.security-review]
related: [integration.webhook.inbound, integration.messaging.api]
sectors: [all]
---

# Outbound Webhook

Enterprise configures their system to send events to a vendor endpoint when data changes. The enterprise is the sender — events flow from the enterprise's system to the vendor when records are created, updated, or deleted.

## Template

- **what:** Webhook configuration in your system to notify us of record changes
- **ready:** We receive a test webhook payload within 5 seconds of a record change in your system

## Matches

Use this type when vendor says: "notify us when things change", "send us events", "real-time updates from your system", "event stream from your CRM/ERP", "outbound webhook"
