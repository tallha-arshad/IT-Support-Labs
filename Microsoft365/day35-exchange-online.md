# Day 35 - Exchange Online Basics

## Key Concepts
Exchange Online is the cloud-hosted email service that powers Microsoft 365 (Outlook). As an IT Helpdesk technician, you will frequently manage mailboxes, create shared inboxes for teams, and set up distribution lists so users can email entire departments at once.

## Lab
Explored the Exchange Admin Center (EAC) and performed core email administration tasks:

- Shared Mailbox Creation: Created a shared mailbox named "Support Team" (support@domain.com). Shared mailboxes allow multiple users to access the same inbox without needing to share a password, which is standard for IT support or customer service teams.
- Distribution List Creation: Created a Distribution List named "All Staff" (allstaff@domain.com) and added a test user to it. Distribution lists are used to send a single email to a group of people without creating a separate mailbox.
- Mailbox Management: Navigated the Recipients tab to view mailboxes, groups, and resources.

## Why It Matters
Managing Exchange Online is a daily task for L1 support. Common tickets include: "I can't access the support inbox" (shared mailbox permissions), "I didn't receive the company-wide email" (distribution list membership), or "My mailbox is full" (storage quotas).

## Interview Q&A

**Q: What is the difference between a shared mailbox and a distribution list?**
A: A shared mailbox has an actual inbox, and multiple users can log in to read and reply to emails from it. A distribution list does not have an inbox; it simply forwards any email sent to it to all of its members.

**Q: How would you give a new employee access to a shared mailbox?**
A: In the Exchange Admin Center, I would go to the shared mailbox's settings, go to Mailbox delegation or Members, and add the new employee with 'Full Access' or 'Send As' permissions.

<img width="1366" height="643" alt="Mailbix-Created" src="https://github.com/user-attachments/assets/e3ad3f12-559d-4d2b-8a64-6cdbda02fa6f" />


<img width="1366" height="643" alt="Exchange-DL-Created" src="https://github.com/user-attachments/assets/6baab3e7-e1b0-4c80-854a-b2576b8337bb" />
