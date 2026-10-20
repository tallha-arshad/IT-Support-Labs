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

<img width="1364" height="768" alt="MS-365-Add-User" src="https://github.com/user-attachments/assets/3be58b40-ec07-4e86-87fa-08931e122fbc" />

<img width="1366" height="768" alt="MS-365-User-added" src="https://github.com/user-attachments/assets/448d36bb-ff77-4411-a686-46b03bb02dfe" />

<img width="1366" height="768" alt="Ms-356-User-in-panel" src="https://github.com/user-attachments/assets/6ebe07c6-4c3e-45cc-919b-ec02260cd9a0" />

