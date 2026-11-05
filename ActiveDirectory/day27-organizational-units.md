# Day 27 - Organizational Units (OUs)

## Key Concepts
Organizational Units (OUs) are containers within Active Directory used to organize users, computers, and groups. They are essential because Group Policy Objects (GPOs) are linked directly to OUs.

## Lab
- Opened "Active Directory Users and Computers" (ADUC).
- Created new OUs for different departments (e.g., Sales, HR, IT).
- Enabled "Protect object from accidental deletion" on each OU.
- Organized test users into their respective departmental OUs.

## Why It Matters
A clean OU structure is required for deploying policies. If a user is in the wrong OU, they will receive the wrong security policies or miss required network drives.

## Interview Q&A
**Q: Why are OUs important?**
A: OUs act as logical folders. They allow IT to apply Group Policies and delegate administrative permissions to specific departments without affecting the entire domain.

<img width="1366" height="720" alt="Capture" src="https://github.com/user-attachments/assets/185ae7a9-c461-4eaf-b267-198f13a46d19" />
