# SSO Implementation – SAML

## Objective
Implement Single Sign-On (SSO) using SAML with Microsoft Entra ID.

---

## Application Setup
- Application Name: IAM Test App - SAML
- Type: Non-gallery Enterprise Application

---

## SAML Configuration
- Identifier (Entity ID): https://iamtestapp.local
- Reply URL (ACS): https://iamtestapp.local/saml

---

## User Assignment
- Assigned User: erick.vargas

---

## Authentication Flow

1. User attempts to access application
2. Application redirects user to Entra ID
3. User authenticates with Entra ID
4. Entra ID sends SAML token to application
5. Application grants access

---

## Key Concepts
- Identity Provider (IdP): Microsoft Entra ID
- Service Provider (SP): IAM Test App
- Protocol: SAML 2.0
