# Day 30 — Week 5 Review: Department Structure in AD

## Key Concepts

Consolidation day for Week 5. No new commands today. The goal is to review the Active Directory environment and ensure it is organized like a real company, with department OUs, users placed in the correct folders, and security groups for each department.

## Lab

Reviewed and organized the AD structure on the Domain Controller:

- Domain: corp.local
- OUs: Sales, HR, IT (and any others created during Week 5)
- Confirmed all users are placed in their correct department OUs
- Confirmed security groups exist for each department (e.g., HR-Team)
- Verified group memberships are correct

The structure in Active Directory Users and Computers (dsa.msc) is now clean, with no users left in the default Users folder. This is the foundational structure required before applying Group Policies in later weeks.

## Why It Matters

A clean AD structure is what makes Group Policy work. If users are scattered or OUs are not organized, policies will hit the wrong people or miss the right ones. This is also the exact setup task an L1 tech handles during onboarding at a real company.

## Interview Q&A

**Q: Walk me through how you'd set up AD for a brand-new 20-person company.**
A: I'd plan the OU structure by department first, decide on a consistent naming convention, then create OUs, users, and security groups matching that plan. Build it methodically, not ad hoc, so it stays manageable as the company grows.

**Q: Why does a consistent naming convention matter in AD?**
A: Without one, accounts and groups become inconsistent and confusing at scale. A clear pattern like firstname.lastname for users and Dept-Team for groups makes searching, auditing, and onboarding dramatically faster.

**Q: Where do Group Policies get applied?**
A: At the OU level. Users and computers inside a linked OU receive the policies attached to that OU. That's why a clean OU structure matters — it determines which policies hit which users.

<img width="981" height="591" alt="day-30-Corp-local-users" src="https://github.com/user-attachments/assets/86754f57-c11e-40aa-acfd-197618fa6906" />
