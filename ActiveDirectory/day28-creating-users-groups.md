# Day 28 - Creating Users & Security Groups

## Key Concepts
User accounts represent individuals who log into the network. Security Groups are collections of users used to assign permissions efficiently. Best practice is to assign permissions to groups, not individual users (Least Privilege).

## Lab
- Created test users within the Sales OU.
- Created a new Security Group named "Sales-Team".
- Added the test users to the Sales-Team group.
- Verified group membership by checking the "Member Of" tab on a user's properties.

## Why It Matters
When a new employee joins, IT simply adds them to the correct group (e.g., Sales-Team) and they instantly inherit all the access they need to shared folders and applications.

## Interview Q&A
**Q: Why use groups instead of assigning permissions directly to users?**
A: Groups simplify administration. If a user changes departments, you just change their group membership. Managing individual permissions for every user is a security risk and doesn't scale.

<img width="1365" height="707" alt="AD-DS-USER-Member-of" src="https://github.com/user-attachments/assets/a5f17ecb-a697-484b-bd0b-416c13c58e16" />
