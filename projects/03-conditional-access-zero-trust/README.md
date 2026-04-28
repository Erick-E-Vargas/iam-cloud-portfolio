# Conditional Access & Zero Trust – Microsoft Entra ID

## 🎯 Objective

Implement Conditional Access policies to enforce secure access controls based on Zero Trust principles.

---

## 📌 Scope

* Conditional Access policy creation
* Multi-Factor Authentication (MFA) enforcement
* User-based access control
* Zero Trust security model implementation

---

## 🧠 Key Concepts

* Conditional Access
* Multi-Factor Authentication (MFA)
* Zero Trust Model
* Policy-based access control
  
---

## 🔐 Conditional Access Policy – MFA for Admins

A Conditional Access policy was created to enforce Multi-Factor Authentication (MFA) for privileged accounts.

### Configuration:
- Users: iam.admin
- Applications: All cloud apps
- Grant Control: Require MFA
- Mode: Report-only

---

## 🧠 Key Insight
Privileged accounts require stronger authentication controls to reduce risk of compromise.

---

## 🚫 Conditional Access Policy – Block High-Risk Sign-Ins

A policy was created to block access when a sign-in is classified as high risk.

### Configuration:
- Users: All users
- Applications: All cloud apps
- Condition: High sign-in risk
- Access Control: Block access
- Mode: Report-only

---

## 🧠 Key Insight
Access decisions should consider risk signals, not just identity. High-risk sign-ins are blocked to prevent potential account compromise.

---

## 🌍 Conditional Access Policy – Location-Based Access Control

A policy was created to restrict access based on geographic location.

### Named Location:
- Trusted Location: Mexico

### Policy Configuration:
- Users: All users
- Applications: All cloud apps
- Condition: Any location excluding trusted location
- Access Control: Block access
- Mode: Report-only

---

## 🧠 Key Insight
Access should be restricted based on geographic risk. Only trusted locations are allowed, reducing exposure to unauthorized access attempts from unknown regions.

---

## 🧪 Policy Validation and Enforcement

Conditional Access policies were initially deployed in report-only mode to evaluate impact without affecting users.

### Validation:
- Sign-in logs were reviewed to analyze policy behavior
- Conditional Access evaluation confirmed expected outcomes

### Enforcement:
- MFA policy for admin accounts was enabled

### Result:
Admin users are now required to complete Multi-Factor Authentication during login.

---

## 🧠 Key Insight
Policies should always be tested in report-only mode before enforcement to prevent unintended access issues.

---


## 🚀 Status

🚧 In progress

