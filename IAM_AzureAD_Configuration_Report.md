
# 🔐 Azure AD Free – IAM Configuration Report

## 📘 Overview
This report documents the Identity and Access Management (IAM) setup using **Azure Active Directory Free Tier**. The goal is to simulate RBAC (Role-Based Access Control) and implement basic security restrictions via conditional access policies.

---

## 🧱 Step 1: Groups Created

| Group Name | Description | Members |
|------------|-------------|---------|
| SOC Analyst | Group for Security Operations Center analysts | testazure1@cyberlab1234.onmicrosoft.com |
| IT Admin | Group for IT administrators | testazure2@cyberlab1234.onmicrosoft.com |

---

## 🧾 Step 2: RBAC (Role-Based Access Control)

Using **built-in roles** only (no custom roles):

| Group Name | Assigned Role | Permissions |
|------------|----------------|-------------|
| SOC Analyst | Security Reader | Read-only access to security-related features |
| IT Admin | User Administrator | Manage users and groups |

---

## 🌐 Step 3: Conditional Access Policy

**Policy Name:** `Restrict Sign-in by IP`

| Setting | Value |
|--------|-------|
| Target Group | SOC Analyst |
| Condition | Location/IP based |
| Included Locations | Any location |
| Excluded Locations | Trusted locations or specific IP range (e.g., `192.168.0.0/24`) |
| Grant Control | Block access or require MFA |
| Status | Enabled |

---

## 🧪 Test Scenario Summary

- Two role-based groups created and assigned to test users.
- Roles applied using Azure built-in roles available in the Free Tier.
- A simple conditional access policy was created to restrict sign-ins by IP address/location.

---

> ✅ This configuration was done entirely within **Azure AD Free Tier**, without requiring Premium P1 licenses.
> 📘 Prepared for cybersecurity education and lab practice in a Microsoft 365 E5 Trial tenant.

