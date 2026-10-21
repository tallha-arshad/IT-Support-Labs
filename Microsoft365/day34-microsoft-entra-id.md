# Day 34 - Microsoft Entra ID (Cloud Identity)

## Key Concepts
Microsoft Entra ID (formerly Azure AD) is the cloud-based identity provider that sits underneath Microsoft 365. It manages users, groups, and authentication (including MFA). While on-premises Active Directory uses Organizational Units (OUs) to organize users, Entra ID relies heavily on Security Groups to manage access to cloud applications. 

## Lab
Explored the Entra ID admin center and performed core identity management tasks:

- **Sign-in Logs (Troubleshooting):** Navigated to Monitoring > Sign-in logs to view authentication attempts. Practiced generating a failed login to understand how to read error codes, IP addresses, and statuses when troubleshooting a user's login issue.
- **Cloud Security Groups:** Created a new cloud-only Security Group named `HR-Team-Cloud`. Added an existing cloud user to the group. This is the standard method for granting access to SaaS applications to multiple users at once.
- **Account Lockout:** Observed how failed login attempts trigger Smart Lockout, and how the "Block Sign-in" toggle in the Admin Center prevents access even with the correct password.

## Why It Matters
Modern companies use Entra ID to manage employee access to thousands of cloud apps. If a user cannot log into Teams or Outlook, the L1 tech checks Entra ID sign-in logs to find the root cause (bad password, MFA failure, or blocked account).

## Interview Q&A

**Q: What is the difference between on-premises Active Directory and Entra ID?**
A: Active Directory is hosted on physical servers and uses OUs and Group Policy to manage local network devices and users. Entra ID is cloud-based and uses Security Groups and Conditional Access to manage access to cloud apps like Microsoft 365.

**Q: If a user is typing the correct password but still can't log in, what is the first thing you check in Entra ID?**
A: I would check the Sign-in logs in Entra ID to see the exact failure reason. It could be a failed MFA prompt, a Conditional Access block (e.g., trying to log in from a foreign country), or an admin might have accidentally checked the "Block sign-in" box.

<img width="1366" height="639" alt="Ms-365-Entra-ID-Sign-in-logs" src="https://github.com/user-attachments/assets/c2706d51-4e71-4693-96f6-c53919beeefd" />


<img width="1366" height="642" alt="Entra-ID-Group-Created-Testuser1-Member" src="https://github.com/user-attachments/assets/faab4aab-539c-4ef8-b5d7-9c00f5ea1609" />
