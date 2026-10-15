# Day 29 — AD PowerShell Cmdlets

## Key Concepts

PowerShell lets you manage Active Directory via commands instead of clicking through the GUI. Useful for bulk operations — creating 20 users at once, or managing group memberships in seconds instead of an hour. Key cmdlets: Get-ADUser (look up users), New-ADUser (create), Set-ADUser (modify), Add-ADGroupMember (add to a group).

## Lab

Ran AD management commands via PowerShell on the Domain Controller:

- `Get-ADUser -Filter *` — listed all users in the domain
- `New-ADUser -Name "Test User 1" -SamAccountName "testuser1" -Enabled $true -AccountPassword (ConvertTo-SecureString "Password123!" -AsPlainText -Force)` — created user 1
- `New-ADUser -Name "Test User 2" -SamAccountName "testuser2" -Enabled $true -AccountPassword (ConvertTo-SecureString "Password1234!" -AsPlainText -Force)` — created user 2
- `Get-ADUser -Filter {Name -like "Test*"} | Format-Table Name, SamAccountName -AutoSize` — verified both users were created
- `Add-ADGroupMember -Identity "HR-Team" -Members "testuser1","testuser2"` — added both users to a security group
- `Get-ADGroupMember -Identity "HR-Team"` — confirmed group membership

All commands executed successfully. Confirmed both new users appear in Active Directory Users and Computers and are now members of the group.

## Why It Matters

Bulk tasks — like onboarding 20 new hires at once — take seconds with a PowerShell script versus an hour of repetitive clicking. Automation skills are increasingly expected even at L1.

## Interview Q&A

**Q: Why would an L1 tech bother learning PowerShell instead of just using the AD GUI?**
A: Because bulk tasks take seconds with a script versus an hour of manual clicking, and automation skills are increasingly expected even at L1.

**Q: What does `Get-ADUser -Filter *` actually do?**
A: It retrieves all user accounts in Active Directory — using `*` as the filter means "match everything."

**Q: What's the difference between `Get-ADUser` and `New-ADUser`?**
A: Get-ADUser reads user information from AD. New-ADUser creates a new user account.

<img width="1366" height="711" alt="Day-29-list-all-users" src="https://github.com/user-attachments/assets/a18c2a25-4b69-4cb2-a23d-46a7964b9a93" />

<img width="1096" height="707" alt="Day-29-2" src="https://github.com/user-attachments/assets/c0b12b3d-b3fa-497a-b8ca-4e76579a7fe6" />
