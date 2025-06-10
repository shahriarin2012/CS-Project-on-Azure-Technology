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

Log in using our Admin email and password

🔹 Step 2: Navigate to 'Users'
In the left-side menu, click on Users

Then select Active users

🔹 Step 3: Add a New User
Click the “+ Add a user” button near the top

*) User#1 Details:
Display name: test azure1 test cs lab1
Username: testazure1@cyberlab1234.onmicrosoft.com
Password: F&443690147500am

*) User#2 Details:
Display name: test azure2 test cs lab2
Username: testazure2@cyberlab1234.onmicrosoft.com
Password: P@439209892725am 

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
Assign or skip training

Choose Launch now

Submit



