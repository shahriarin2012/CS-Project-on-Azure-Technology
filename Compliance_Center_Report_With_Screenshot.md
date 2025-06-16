
# 🧾 Microsoft Compliance Center – Exploration Report (with Live Example)

## 📘 Overview
This report captures the exploration of Microsoft Compliance Center to assess the compliance score, simulate data exfiltration detection using DLP (Data Loss Prevention) policies, and explore Information Protection labels. This was performed using a Microsoft 365 E5 trial account.

---

## 🔐 Step 1: Access Microsoft Compliance Center

1. Navigate to 👉 [https://compliance.microsoft.com](https://compliance.microsoft.com)
2. Sign in as **admin@yourlab1234.onmicrosoft.com**
3. You will land on the **Overview Dashboard**

---

## 📊 Step 2: Check Compliance Score

- **Compliance Score Observed:** `56%`
- **Points Achieved:** `12,345/21,739`
- **Microsoft Managed Points:** `12,345/12,438`
- **Your Points:** `0/9,301`

### Key Improvement Actions (examples):
| Action | Status | Points | Risk |
|--------|--------|--------|------|
| Control data by restricting cloud access | ❌ Failed high risk | 27 | High |
| Implement anti-malware policies | ⏳ Not completed | 27 | - |

### Solution Score Breakdown:
| Solution | Score | Remaining Actions |
|----------|-------|--------------------|
| Data Loss Prevention | 0/361 points | 15 |
| Exchange Online | 0/167 points | 9 |
| Azure | 0/112 points | 6 |

✅ Screenshot captured from live portal with real-time score summary.

---

## 🛡️ Step 3: Simulate DLP Policy for Data Exfiltration

1. In Compliance Center left menu → **Data loss prevention**
2. Click **+ Create Policy**
3. Select **Custom Policy** and name it: `Sim-Test-DLP-Exfiltration`
4. Choose locations like **Exchange, OneDrive, Teams**
5. Set detection condition: 
   - Sensitive Info Type = **Credit Card Numbers**
6. Action = **Audit Only** (Simulated Detection)
7. Enable alerts to Admin

📩 You can simulate by sending a test email with fake sensitive info:
`4111 1111 1111 1111` → This may trigger a test alert

---

## 🔖 Step 4: Explore Information Protection Labels

1. Go to **Information Protection** → **Labels**
2. Click **+ Create a Label**
3. Name: `Confidential - Internal`
4. Apply:
   - Encryption
   - External sharing restrictions
   - Watermarks or headers
5. Publish to test users via label policy

✅ These labels help classify, protect, and control sensitive content.

---

## ✅ Summary of Tasks Performed

| Task | Status |
|------|--------|
| Checked Compliance Score (56%) | ✅ |
| Reviewed top recommendations | ✅ |
| Created a custom DLP policy to simulate exfiltration detection | ✅ |
| Created and published sensitivity label | ✅ |

---

> 🧠 Microsoft Compliance Center is essential for security and compliance professionals to protect data, prevent leaks, and follow industry regulations. This exercise introduces practical policy creation and label-based classification.
