# Azure M365 Defender Security Lab – Free Tier Edition

## Objective

Learn core cybersecurity skills using **Microsoft 365 Defender**, **Azure IAM**, and **Microsoft Sentinel**, all using free-tier tools.

## Tools Used

- Microsoft 365 Defender (via Dev Program)
- Azure AD Free Tier
- Microsoft Sentinel (free log ingestion)
- Compliance Center


# SetUp MS 365 Defender
1)Microsoft 365 Defender
2)25 dummy users
![image](https://github.com/user-attachments/assets/890609df-da19-4927-a1bf-08f799c17510)

# Create Dummy/Test Users in Microsoft 365 Admin Center
✅ Pre-Requisite
We must need Admin Access to your Microsoft 365 tenant.

🔹 Step 1: Go to Microsoft 365 Admin Center
Open your browser and go to 👉 https://admin.microsoft.com

Log in using our Admin email and password ( admin@cyberlab1234.onmicrosoft.com /  ****d**!)

🔹 Step 2: Navigate to 'Users'
In the left-side menu, click on Users

Then select Active users

🔹 Step 3: Add a New User
Click the “+ Add a user” button near the top

*) User#1 Details:
Display name: test azure1 test cs lab1
Username: testazure1@cyberlab1234.onmicrosoft.com
Password: F&443690147500am/ ****d!

*) User#2 Details:
Display name: test azure2 test cs lab2
Username: testazure2@cyberlab1234.onmicrosoft.com
Password: P@439209892725am / ****d!

*) User#3 Details:
Display name: test azure3 test cs lab3
Username: testazure3@cyberlab1234.onmicrosoft.com
Password: R#838964183493an

*)Regular user:
Username: qatester@cyberlab1234.onmicrosoft.com
password: *****d!


Admin User:
Display name: admin
Username: admin@cyberlab1234.onmicrosoft.com
Password: W(643891120169os / ***d!

![alt text](image.png)

# Launch a Phishing Simulation Campaign



![image](https://github.com/user-attachments/assets/7dcc435a-1198-4e57-ab5a-c489b4eef6d1)

In Microsoft Defender’s Attack Simulation Training, "Phishing" is the general category — but when you go into the simulation setup, it offers specific attack techniques that simulate different types of phishing attacks.

🎯 What We are Seeing = Phishing Techniques (Subtypes)
Here’s what each option means:

Credential Harvest	Sends a fake login page to steal usernames/passwords	✅ Yes	✅ Best option for beginner simulation
Malware Attachment	Sends a malicious file as an attachment	✅ Yes	Good for advanced cases
Link in Attachment	Email has an attachment that contains a malicious link	✅ Yes	
Link to Malware	A link in the email directly downloads malware	✅ Yes	
Drive-by URL	A link that silently tries to exploit the browser	✅ Yes	
OAuth Consent Grant	Tricks user into giving access to apps via OAuth	✅ Yes	
How-to Guide	Just an informational help guide (not a technique)	❌ No	Just for reference

✅ Best Option for My Assignment
Select:
🔹 Credential Harvest

Why?
It simulates a fake login page (like Outlook or Microsoft login)

It's the most common phishing method

Easy to track: users click the link → enter dummy credentials → results show up in your dashboard

📌 What to Do Now:
Select Credential Harvest

Click Next

Continue the rest of the simulation setup:

Name the simulation

Choose a payload/template (e.g., fake Microsoft login)

Select your test users (like AdeleV, MiriamG)



# Adding my Target Users
![image](https://github.com/user-attachments/assets/90c8a6ac-d570-4a5f-aab2-861b4ebb85a0)


Now, 
# Select Phishing Landing Page
![image](https://github.com/user-attachments/assets/410c9314-6bd2-4d7e-ae32-d99c35b92357)



![image](https://github.com/user-attachments/assets/91a761de-c761-46ac-bf66-cb1c40abe016)

![image](https://github.com/user-attachments/assets/c186d4a8-960f-42fd-b277-87706dd00f2c)

![image](https://github.com/user-attachments/assets/bc101b71-cf94-4416-9069-2506fc40aebe)



# Choose Launch now / Send a test

![image](https://github.com/user-attachments/assets/2cf37fe5-e29b-429c-9ec0-aed202aa9a25)





# Now Send test email and login as those test users

![image](https://github.com/user-attachments/assets/79e3dd3a-0213-4325-9c02-07b80987c71d)



# Submit

![image](https://github.com/user-attachments/assets/5cd3fdc2-f6a9-4c2e-84f5-adf9c1eea817)


✅ What Happened After Submission
The phishing simulation is scheduled to:

Start: June 10, 2025, at 2:03 AM

Targets: 3 users

✅ Technique: Credential Harvest

✅ Status: Scheduled

🕒 What Happens Next
Within a few minutes (or at the scheduled time), each of the target users will receive a phishing email (e.g., a fake Microsoft login or password alert).

👣 What We Should Do Next
🔹 Step 1: Log in as One of the Test Users 
Pick one of the test users you targeted. Example:

( logged in as Test Azure1 test CS Lab1)

How to Log In:
Lets Go to 👉 https://outlook.office.com

Enter the user’s email and password

Open their inbox

Look for the phishing simulation email

Click the phishing link

![image](https://github.com/user-attachments/assets/ab844945-92cb-42d8-a947-affb18732f36)



🔹 Step 2: Go Back to Admin Dashboard and Track
Go to: https://security.microsoft.com/attacksimulator

Click on your campaign name ( Phishing )

We’ll see:

✅ Who clicked the link

✅ Who submitted credentials

✅ Whether Microsoft Defender detected the attack

✅ If auto-remediation actions (like email removal) were taken


![image](https://github.com/user-attachments/assets/ae842ae5-6672-4783-a16f-84cfc28914b4)

# ----------------------------------------------------------------------------------------------------

# 4: Configure IAM (Identity and Access Management) with Azure AD Free

🎯 Goal:
Set up IAM (Identity and Access Management) using Azure Active Directory (Azure AD Free). This includes:

Creating user groups like SOC Analyst and IT Admin

Assigning RBAC (Role-Based Access Control) using built-in roles

Setting up a Conditional Access policy (e.g., IP/location restriction)



🛠️ Prerequisites:
Before starting, we have to make sure:

We’re signed in as the Global Administrator (the admin account you created earlier — e.g., admin@shahriar143.onmicrosoft.com )

We have access to the Azure Portal: https://portal.azure.com


🧭 Step-by-Step Instructions
🔹 Step 1: Go to Azure Active Directory
Open browser and go to 👉 https://portal.azure.com

Sign in with your admin credentials ( admin@shahriar143.onmicrosoft.com /  **** d***!)

In the left-side menu, click on “Microsoft Entra" --> WHich is new name for Azure Active Directory

![image](https://github.com/user-attachments/assets/04b4a74c-e443-4449-9fb5-90bc20089383)


✅ We're now in the Azure AD control center



# 🔹 Step 2: Create New Groups
We will create two groups:

SOC Analyst

IT Admin

🔸 How to Create Each Group:
In Azure AD, click “Groups”

Click + New group

Now fill in the form:

Field	Value
Group type	Security
Group name	SOC Analyst
Group description	Group for Security Operations Center analysts
Membership type	Assigned
Members	Click “No members selected” and choose 1–2 test users (e.g., testazure1)


Click Create


![image](https://github.com/user-attachments/assets/456169a0-bd84-49b3-9910-80de262424a6)

![image](https://github.com/user-attachments/assets/dda7c9aa-2f62-40d0-a439-f71f8f1a4533)






📌 We will repeat these steps again to create the "IT Admin" group.

![image](https://github.com/user-attachments/assets/16f908bb-d3d9-4824-9074-f0d309bbf443)


🔹 Step 3: Assign RBAC (Role-Based Access Control) Using Built-in Roles
✅ Why Built-in Only?
Azure AD Free doesn’t support custom roles — we can only use built-in roles like:

User Administrator

Security Reader

Global Reader

Intune Administrator

🔸 Assign a Role to a Group

Go back to Azure AD home

Click “Roles and administrators”
![image](https://github.com/user-attachments/assets/a3ec16e3-d177-4e7c-8d7a-fb115a7873b1)


Scroll and choose a role like:

Security Reader → good for SOC Analyst

![image](https://github.com/user-attachments/assets/98803c56-ed91-4175-acd7-58fffceab740)


User Administrator or Intune Administrator → for IT Admin

![image](https://github.com/user-attachments/assets/ad08e1b2-499d-4953-8dc6-25398028deeb)






Click the role name (e.g., Security Reader)

Click + Add assignments
![image](https://github.com/user-attachments/assets/23b1b4be-d866-4413-b848-1dbad6f14d6a)


In the Add Assignment panel:

Search and select SOC Analyst group

Click Add

📌 Repeat for the IT Admin group using a different role.

![image](https://github.com/user-attachments/assets/7db4016b-ca59-48a3-ac37-0b28c8b77aaf)





🔹 Step 4: Configure Basic Conditional Access Policy (IP/Location Restriction)
✅ Even though Conditional Access is mostly a Premium P1 feature, you can create 1 basic policy in free tenants for learning/demo purposes.

🔸 How to Create a Basic Policy:
In Azure AD, go to Security → Conditional Access

Click + New policy
![image](https://github.com/user-attachments/assets/bf1600a3-3881-4a05-bc69-00176e9f2d1f)


Give it a name: Restrict Sign-in by IP


Under Assignments → Users or workload identities

Click Select users and groups


Select SOC Analyst group

![image](https://github.com/user-attachments/assets/e48c5db7-8b8a-4904-8138-5be7c6c5ed72)

Under Assignments → Conditions → Locations
![image](https://github.com/user-attachments/assets/22187be8-0f46-41ec-a356-3bfb79eed09f)


Enable Configure → Choose Yes

Click Include → Select Any location

Click Exclude → Select Trusted locations or add specific IPs (e.g., 192.168.0.0/24)

Under Access Controls → Grant

Choose Block access OR Require MFA

Click Enable Policy → On

![image](https://github.com/user-attachments/assets/f17e059f-91a5-4e44-bbbf-8af336bee9a7)

System will ask to disable default security - Let's do it 

![image](https://github.com/user-attachments/assets/29d8c60c-2ed8-436d-b828-8fa2f447c3e3)


Click Create
![image](https://github.com/user-attachments/assets/f4effbe3-b4fc-4887-ac7a-d7036fb6e78b)

![image](https://github.com/user-attachments/assets/38d08c78-a20a-48cb-b998-67f91efe17f4)

# ----------------------------------------------

🧪 Example Scenario:

Groups:

SOC Analyst → assigned to Security Reader role

IT Admin → assigned to User Administrator role

Conditional Access Policy:

Blocks SOC Analyst users from logging in unless they're from a trusted location/IP

✅ Summary / Conclusion: 
Task	Completed
Created SOC Analyst group	✅
Created IT Admin group	✅
Assigned built-in roles (RBAC)	✅
Created conditional access policy	✅


# # Task # 5 :🛡️ Microsoft Sentinel Setup Report – Free Ingestion

## 📘 Overview
This guide documents how to set up Microsoft Sentinel using the free tier, connect key data sources, and create a basic alert rule. Sentinel enables Security Information and Event Management (SIEM) in the cloud for detecting and responding to threats.

---

## 🧱 Step 1: Create a Log Analytics Workspace

1. Go to 👉 [https://portal.azure.com](https://portal.azure.com)
2. Search **“Log Analytics workspaces”** in the top search bar.
3. Click **+ Create**.

![image](https://github.com/user-attachments/assets/33269daf-1ca2-4bce-b088-d5e427362a0f)
![image](https://github.com/user-attachments/assets/44aa4e50-ccf0-459b-aed3-069c886fd9a1)



4. Fill the form:
   - **Subscription:** Select your active subscription
   - **Resource Group:** Create new (e.g., `SentinelLabRG`)
   - **Name:** `SentinelWorkspace`
   - **Region:** Choose closest to you (e.g., East US)

 5. Click **Review + Create**, then **Create**

![image](https://github.com/user-attachments/assets/8532bdda-79a6-4574-a007-942647553deb)


--Click Create and the deployment will begin. Wait till the Deployment is complete.

![image](https://github.com/user-attachments/assets/94da0a07-70dd-4830-b434-8f4092c9090e)
---

## 🔧 Step 2: Enable Microsoft Sentinel on the Workspace

1. Go back to the main portal dashboard
2. Search **"Microsoft Sentinel"**
3. Click **+ Add** → Select the workspace `SentinelWorkspace`



![image](https://github.com/user-attachments/assets/1076ee99-88aa-4b51-a6fe-14fd3316c27f)


4. Click **Add Microsoft Sentinel**

![image](https://github.com/user-attachments/assets/cda55b3a-6755-4a5b-b241-d14c8b2bc3b5)

---

## 🔗 Step 3: Connect Data Sources

### 🔹 a) Connect Microsoft 365 Defender

1. In Sentinel, click **Data connectors**

![image](https://github.com/user-attachments/assets/f949b0ef-a8c5-42d7-9bbe-67fec335dab3)



2. Search for **“Microsoft 365 Defender”**

![image](https://github.com/user-attachments/assets/24be31d7-975f-44bc-9c6d-e9543f2347b8)


![image](https://github.com/user-attachments/assets/6085fafc-6f02-44a1-954a-6d7d39c9c9d7)


Select MicroSoft Entra ID 


3. Click on it → Click **Open connector page**
4. Click **Connect** (you may need to grant permissions)
5. Follow instructions to complete connection

### 🔹 b) Connect Azure Activity Logs

1. Back in **Data connectors**, search **Azure Activity**
2. Click **Open connector page**
3. Enable log collection → **Connect**

✅ You are now collecting logs from Defender and Azure.
















