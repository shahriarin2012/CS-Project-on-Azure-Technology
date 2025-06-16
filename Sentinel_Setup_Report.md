
# 🛡️ Microsoft Sentinel Setup Report – Free Ingestion

## 📘 Overview
This guide documents how to set up Microsoft Sentinel using the free tier, connect key data sources, and create a basic alert rule. Sentinel enables Security Information and Event Management (SIEM) in the cloud for detecting and responding to threats.

---

## 🧱 Step 1: Create a Log Analytics Workspace

1. Go to 👉 [https://portal.azure.com](https://portal.azure.com)
2. Search **“Log Analytics workspaces”** in the top search bar.
3. Click **+ Create**.
4. Fill the form:
   - **Subscription:** Select your active subscription
   - **Resource Group:** Create new (e.g., `SentinelLabRG`)
   - **Name:** `SentinelWorkspace`
   - **Region:** Choose closest to you (e.g., East US)
5. Click **Review + Create**, then **Create**

---

## 🔧 Step 2: Enable Microsoft Sentinel on the Workspace

1. Go back to the main portal dashboard
2. Search **"Microsoft Sentinel"**
3. Click **+ Add** → Select the workspace `SentinelWorkspace`
4. Click **Add Microsoft Sentinel**

✅ Microsoft Sentinel is now active on your workspace.

---

## 🔗 Step 3: Connect Data Sources

### 🔹 a) Connect Microsoft 365 Defender

1. In Sentinel, click **Data connectors**
2. Search for **“Microsoft 365 Defender”**
3. Click on it → Click **Open connector page**
4. Click **Connect** (you may need to grant permissions)
5. Follow instructions to complete connection

### 🔹 b) Connect Azure Activity Logs

1. Back in **Data connectors**, search **Azure Activity**
2. Click **Open connector page**
3. Enable log collection → **Connect**

✅ You are now collecting logs from Defender and Azure.

---

## 🔔 Step 4: Create a Simple Analytics Rule

### 🔹 Goal: Create an alert for “Phishing Click Event”

1. In Sentinel → Go to **Analytics** (left panel)
2. Click **+ Create → Scheduled query rule**

Fill the setup:

### 📝 Rule Details:
- **Name:** Phishing Click Alert
- **Severity:** Medium
- **Tactics:** Initial Access

### 🔍 Set Rule Logic:

In the **Query** section, paste the following sample:

```kusto
EmailEvents
| where ThreatType == "Phish" and DeliveryAction == "Clicked"
```

This is a simple KQL (Kusto Query Language) query that detects phishing click events.

### 🛎️ Set Alert Details:
- **Alert rule frequency:** Every 5 minutes
- **Lookup data source:** SentinelWorkspace

Click **Next** through all tabs and finally click **Create**

---

## 🧪 Test Summary

- Created and configured Microsoft Sentinel
- Connected Microsoft 365 Defender and Azure Activity
- Built a working alert rule that detects phishing click events from email logs

---

> 🧠 This setup helps build THE foundation in SIEM. The ingestion is free for specific data sources like Defender and Azure Activity Logs under the free plan.

