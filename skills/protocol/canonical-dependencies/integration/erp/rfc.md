---
id: integration.erp.rfc
name: SAP RFC/BAPI Access
category: integration
systems: [sap]
requires: [auth.service-account, stakeholder.technical-lead]
blocked_by: [process.security-review, process.architecture-review]
related: [integration.erp.api, data.field-mapping]
sectors: [manufacturing, retail, financial-services]
---

# SAP RFC/BAPI Access

Direct SAP RFC (Remote Function Call) and BAPI (Business API) connectivity for real-time transaction processing. More complex than REST API integration — requires SAP-specific connectivity, middleware (e.g., SAP Cloud Connector), and deeper enterprise coordination.

## Template

- **what:** SAP RFC connectivity for real-time transaction processing
- **ready:** We can execute a test BAPI call and receive response data

## Matches

Use this type when vendor says: "SAP RFC", "BAPI calls", "SAP connector", "direct SAP access", "SAP Cloud Connector", "RFC destination"
