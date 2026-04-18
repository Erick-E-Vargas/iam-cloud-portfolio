# IAM Core Concepts (Engineering Reference)

## Authentication vs Authorization
- Authentication: Verifying identity (who you are)
- Authorization: Determining access (what you can do)

---

## SAML (Security Assertion Markup Language)
- Enterprise SSO protocol
- XML-based assertions
- Common in SaaS integrations (Salesforce, ServiceNow)

---

## OAuth 2.0
- Authorization framework
- Used for API access delegation
- Does NOT handle authentication alone

---

## OpenID Connect (OIDC)
- Identity layer built on OAuth 2.0
- Used for modern authentication flows
- Returns ID tokens (JWT)

---

## Hybrid Identity
- Integration between on-prem Active Directory and Microsoft Entra ID
- Enables centralized identity management across cloud and on-prem systems
