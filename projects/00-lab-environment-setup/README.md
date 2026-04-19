# Lab Environment Setup

## 🎯 Objective
Build a clean IAM lab environment to simulate enterprise hybrid identity using Active Directory and Microsoft Entra ID.

---

## 🏗️ Architecture

On-Prem (Hyper-V)
- DC01 (Windows Server 2022)
- Domain: iamlab.local

Cloud
- Microsoft Entra ID Tenant
- Domain: eviamlab.onmicrosoft.com
- Display Name: IAM Lab – Erick Vargas

---

## 🧱 Environment Components

- Hyper-V (local virtualization)
- Windows Server 2022 (Domain Controller)
- Microsoft Entra ID (Azure AD tenant)

---

## 🏷️ Naming Standards

### On-Prem Active Directory
- Domain: iamlab.local
- Domain Controller: DC01

### Cloud (Entra ID)
- Tenant Domain: eviamlab.onmicrosoft.com
- Tenant Name: IAM Lab - Erick Vargas

---

## 📝 Windows Server Setup (Summary)

A Windows Server 2022 virtual machine was deployed using Hyper-V and configured with the hostname DC01.

Detailed OS installation steps are omitted as they are standard and not IAM-specific.

---

## 🔧 Active Directory Domain Services Installation

The Active Directory Domain Services (AD DS) role was installed on DC01 using Server Manager.

At this stage, the server is prepared for promotion to a Domain Controller, where the Active Directory forest will be created.

---

## 🧪 Active Directory Domain Creation

DC01 was promoted to a Domain Controller, creating a new Active Directory forest.

- Domain: iamlab.local
- NetBIOS Name: IAMLAB
- Roles: DNS, Global Catalog

This establishes the core identity system for the hybrid IAM environment.

---

## 🧱 IAM OU Structure Implementation

A structured IAM model was implemented inside Active Directory under the IAM OU.

### Sub-OUs Created:
- Users (standard identities)
- Admins (administrative identities)
- Service Accounts (system identities)
- Groups (authorization layer)
- Workstations (endpoint identity layer)

### Initial User Accounts:
- erick.vargas (standard user)
- test.user1 (test user)
- iam.admin (privileged user in Domain Admins)

This structure follows enterprise IAM design principles including separation of duties and role-based access control (RBAC).

---

## ☁️ Hybrid Identity Setup (Microsoft Entra Connect)

Microsoft Entra Connect was installed on DC01 to enable synchronization between on-premises Active Directory and Microsoft Entra ID.

### Configuration:
- Sync Type: Password Hash Synchronization (PHS)
- Scope: IAM OU
- Source: iamlab.local
- Target: eviamlab.onmicrosoft.com

### Result:
On-premises user accounts are now synchronized to Microsoft Entra ID, enabling hybrid identity management.

---

## 🔄 Hybrid Identity Validation

User accounts synchronized from Active Directory are now visible in Microsoft Entra ID, confirming successful hybrid identity configuration.

This validates end-to-end identity provisioning:

On-Prem AD → Entra Connect → Microsoft Entra ID

Authentication layer (SSO, SAML, OAuth, OIDC) will be implemented in the next phase.

---

## 🧠 Notes

This environment will be used to simulate:
- Hybrid identity (AD → Entra ID)
- Identity synchronization
- Enterprise authentication scenarios
