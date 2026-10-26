# Day 21 - Installing Windows Server (ISO, Setup Steps)

## Key Concepts
Windows Server is Microsoft's enterprise operating system used to run Active Directory, DNS, and file shares. During installation, you must choose between "Desktop Experience" (with a GUI) and "Server Core" (command-line only). We use Desktop Experience for learning.

## Lab
- Booted the VM with the Windows Server ISO attached.
- Followed the setup wizard: selected language, clicked "Install Now".
- Chose "Windows Server Standard Evaluation (Desktop Experience)".
- Accepted the license terms and chose "Custom Install".
- Selected the 60GB virtual hard drive and waited for the files to copy.
- Set the local Administrator password and logged into the Server Manager dashboard.

## Why It Matters
Installing Windows Server is the foundation of building a domain. Most corporate environments run on Windows Server, so hands-on installation experience is a mandatory L1/L2 skill.

## Interview Q&A

**Q: What is the difference between Server Core and Desktop Experience?**
A: Server Core has no graphical interface and is managed entirely via command line or remote tools, saving resources. Desktop Experience includes the full Windows GUI, making it easier for beginners to navigate.

<img width="1365" height="730" alt="Server-installation-on-VMware" src="https://github.com/user-attachments/assets/40e3ad62-4e50-4d4b-b5a4-5f971b2536d0" />

