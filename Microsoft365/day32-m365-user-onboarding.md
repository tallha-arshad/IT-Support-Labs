# Day 32 - M365 User Onboarding & Licensing

## Key Concepts
Onboarding a new employee in Microsoft 365 requires creating their account and assigning them a license. Without a license, they cannot access Outlook, Teams, or SharePoint. The Principle of Least Privilege dictates that standard users should not have admin access.

## Lab
- Navigated to Active Users and clicked "Add a user".
- Created "Test User 1" with a custom password.
- Assigned the Microsoft 365 Business Basic license.
- Ensured the role was set to "User (no admin center access)" to follow the Principle of Least Privilege.

## Why It Matters
This is the exact process used when a company hires a new employee. The L1 tech is usually the one responsible for creating the account and getting the user set up on day one.

## Interview Q&A
**Q: What happens if you create a user but forget to assign a license?**
A: The user will be created in Active Directory, but they will not have access to any Microsoft 365 services like Outlook, Teams, or OneDrive. They will get an error when trying to log in.

<img width="1364" height="768" alt="MS-365-Add-User" src="https://github.com/user-attachments/assets/626e2af3-e092-49d3-a662-99ef1793b6c2" />

<img width="1366" height="768" alt="MS-365-User-added" src="https://github.com/user-attachments/assets/4ec3a6e7-b8e9-4b8b-b965-1d5039e13346" />

<img width="1366" height="768" alt="Ms-356-User-in-panel" src="https://github.com/user-attachments/assets/a41ac26a-7e00-49b8-b360-5795fd4dc266" />
