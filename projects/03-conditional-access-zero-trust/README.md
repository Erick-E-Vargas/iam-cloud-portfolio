# Conditional Access & Zero Trust – Microsoft Entra ID

## 🎯 Objective

Implement Conditional Access policies to enforce secure access controls based on Zero Trust principles, including MFA, risk-based, and location-based access.

---

## 📌 Scope

* Conditional Access policy creation
* Multi-Factor Authentication (MFA) enforcement
* Risk-based access control
* Location-based access control
* Policy validation and safe enforcement

---

## 🧠 Key Concepts

* Conditional Access
* Multi-Factor Authentication (MFA)
* Zero Trust Model
* Policy-based access control
* Risk-based authentication

---

## 🔐 Conditional Access Policies

### 1. MFA for Admin Accounts

* **Users:** iam.admin
* **Applications:** All cloud apps
* **Control:** Require MFA
* **Mode:** Enforced

![MFA Policy](screenshots/01-mfa-policy.png)

---

### 2. Block High-Risk Sign-Ins

* **Users:** All users
* **Applications:** All cloud apps
* **Condition:** High sign-in risk
* **Control:** Block access
* **Mode:** Report-only

![Risk Policy](screenshots/02-block-high-risk.png)

---

### 3. Location-Based Access Control

* **Named Location:** Trusted Location - Mexico
* **Users:** All users
* **Applications:** All cloud apps
* **Condition:** Any location excluding trusted location
* **Control:** Block access
* **Mode:** Report-only

![Named Location](screenshots/03-named-location.png)
![Location Policy](screenshots/04-location-policy.png)

---

## 🧪 Validation and Testing

Policies were first deployed in report-only mode to evaluate their impact without affecting users.

### Validation Steps:

* Reviewed sign-in logs
* Analyzed Conditional Access evaluation results

![Sign-in Logs](screenshots/05-signin-logs-report-only.png)

---

## 🚀 Enforcement

The MFA policy for admin accounts was enabled and tested.

### Result:

* Admin users are required to complete MFA during login

![MFA Enforcement](screenshots/06-mfa-enforcement.png)

---

## 🧠 Zero Trust Model

This implementation follows Zero Trust principles:

* Never trust by default
* Always verify identity
* Evaluate risk and context before granting access

---

## 📊 Architecture Diagram

![Zero Trust Flow](diagrams/zero-trust-conditional-access.png)

---

## 🧠 Key Insights

* Access decisions should consider identity, location, and risk
* Policies should be tested before enforcement
* Privileged accounts require stronger controls
* Conditional Access is central to Zero Trust architecture

---

## 📅 Execution Timeline

* Implemented: April 2026

---

## 🚀 Status

✅ Completed
