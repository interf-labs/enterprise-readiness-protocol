---
id: auth.sso.oidc
name: SSO via OIDC
category: auth
systems: [okta, azure-ad, auth0, ping-identity, google-workspace]
requires: []
blocked_by: [process.security-review]
related: [auth.sso.saml, auth.api-credentials]
sectors: [all]
---

# SSO via OIDC

Enterprise SSO integration using OpenID Connect protocol. More common with modern and cloud-native enterprises than SAML. Vendor's application authenticates users through the enterprise identity provider using OIDC flows.

## Template

- **what:** OIDC endpoint for our service to authenticate your users
- **ready:** A test user can complete the OIDC flow and access our application

## Matches

Use this type when vendor says: "OIDC integration", "OpenID Connect", "OAuth2 login", "modern SSO", "OIDC provider", "JWT-based authentication"
