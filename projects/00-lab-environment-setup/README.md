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
- Tenant Name: IAM Lab – Erick Vargas

---

## 📝 Windows Server Setup (Summary)

A Windows Server 2022 virtual machine was deployed using Hyper-V and configured with the hostname DC01.

Detailed OS installation steps are omitted as they are standard and not IAM-specific.

---

## 🧠 Notes

This environment will be used to simulate:
- Hybrid identity (AD → Entra ID)
- Identity synchronization
- Enterprise authentication scenarios
