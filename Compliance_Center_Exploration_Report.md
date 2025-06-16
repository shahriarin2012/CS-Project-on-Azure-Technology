
# 🧾 Microsoft Compliance Center – Exploration Report

## 📘 Overview
This guide documents how to explore the Microsoft Compliance Center to monitor organizational compliance, simulate data loss prevention alerts, and inspect sensitivity labels for information protection. This was performed using a Microsoft 365 E5 trial tenant.

---

## 🔐 Step 1: Access Microsoft Compliance Center

1. Open your browser and go to 👉 [https://compliance.microsoft.com](https://compliance.microsoft.com)
2. Sign in using your **admin@yourlab1234.onmicrosoft.com** account
3. You’ll land on the **Compliance Center Dashboard**

---

## 📊 Step 2: Check Compliance Score

1. On the homepage/dashboard, you’ll see **Compliance Score** (e.g., 27.6%).
2. Click on it to explore:
   - Improvement actions
   - Product-specific recommendations
   - Overall progress

This score reflects how well your organization is meeting Microsoft’s compliance standards.

---

## 🛡️ Step 3: Explore DLP (Data Loss Prevention) Policies

### 🔹 Goal: Simulate data exfiltration alert

1. In the left panel, go to **Data loss prevention**
2. Click **+ Create policy**
3. Choose **Custom Policy** → Click **Next**
4. Name it: `DLP - Test Data Exfiltration`
5. Choose **Locations**:
   - Select **Exchange email**, **OneDrive**, **Teams** if enabled
6. Choose **Conditions**:
   - Look for “Credit Card Numbers” or “Sensitive Info Types”
7. Set the **action** to:
   - **Audit only** (for simulation)
   - **Send alert to admin**

8. Assign to all or specific users (e.g., `testazure1`)
9. Click **Create** and allow 15–30 mins to become active

✅ Once active, send a test message or upload a file containing fake sensitive data (like `4111 1111 1111 1111`) to simulate detection.

---

## 🔖 Step 4: Explore Information Protection Labels

1. In the left menu, go to **Information protection**
2. Under **Labels**, click **+ Create a label**
3. Name it: `Confidential - Internal`
4. Description: “Internal use only – do not share externally”
5. Choose what the label does:
   - Encrypt files
   - Prevent external sharing
   - Watermark or mark content
6. Publish the label via a **label policy** to test users

✅ You now have an applied sensitivity label in your tenant.

---

## 🧪 Summary of Tasks Performed

| Task | Status |
|------|--------|
| Accessed Microsoft Compliance Center | ✅ |
| Reviewed Compliance Score | ✅ |
| Created DLP Policy for simulation | ✅ |
| Created and published sensitivity label | ✅ |

---

> 🧠 Exploring the Compliance Center teaches how to monitor organizational risk, prevent data leakage, and apply information governance policies — key skills for cybersecurity and compliance roles.
