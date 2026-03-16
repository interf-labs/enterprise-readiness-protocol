---
id: integration.analytics.api
name: Analytics & Data Warehouse
category: integration
systems: [snowflake, databricks, bigquery, redshift, mixpanel, amplitude, tableau, looker]
requires: [auth.api-credentials, stakeholder.data-team]
blocked_by: [process.security-review]
related: [data.field-mapping, data.sample-dataset]
sectors: [all]
---

# Analytics & Data Warehouse

Vendor needs access to enterprise analytics or data warehouse for reporting, enrichment, or building models on behavioral data.

## Template

- **what:** API access to your analytics platform for usage data and reporting
- **ready:** We can execute a test query against your analytics platform and receive results

## Matches

Use this type when vendor says: "access to your analytics", "usage data", "event tracking system", "Mixpanel/Amplitude/Snowflake access", "data warehouse query access", "BI platform"
