# Day 26 - Promoting a Server to a Domain Controller

## Key Concepts
A Domain Controller (DC) is a server that runs Active Directory. Promoting a server to a DC means installing the AD DS role and configuring it to host the domain database.

## Lab
- Added the "Active Directory Domain Services" role in Server Manager.
- Ran the Active Directory Domain Services Configuration Wizard.
- Selected "Add a new forest" and named the root domain (e.g., corp.local).
- Set the DSRM (Directory Services Restore Mode) password.
- Completed the installation and restarted the server.

## Why It Matters
The DC is the brain of the network. It authenticates every user and computer that tries to access domain resources. 

## Interview Q&A
**Q: What is the DSRM password used for?**
A: DSRM (Directory Services Restore Mode) is used for disaster recovery. If Active Directory becomes corrupted, this password allows an admin to boot the server into a special recovery mode to restore the database.

<img width="1366" height="720" alt="Capture" src="https://github.com/user-attachments/assets/214fdd71-c467-4f23-8fd6-73e6ff90573b" />
