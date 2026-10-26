# Day 19 - Installing VirtualBox & Creating Your First VM

## Key Concepts
VirtualBox is a free Type 2 Hypervisor that allows you to run a full operating system (like Windows Server) inside your own computer as a Virtual Machine (VM). This lets you build enterprise labs and test configurations without needing physical hardware. 

## Lab
- Downloaded and installed VirtualBox from the official website.
- Downloaded a Windows Server evaluation ISO (180-day trial) from Microsoft.
- Created a new VM named "DC01" and selected Windows Server 2019/2022 (64-bit) as the version.
- Allocated 4GB of RAM and 2 CPU cores to the VM.
- Created a 60GB dynamically allocated virtual hard disk.
- Attached the Windows Server ISO to the VM's optical drive.
- Started the VM and successfully booted into the Windows Server installation screen.

## Why It Matters
Virtualization is how real IT departments test changes safely. You can break a VM, revert to a snapshot, and start over in seconds. Knowing how to build a VM is a core skill for any IT Support role.

## Interview Q&A

**Q: What is a hypervisor?**
A: A hypervisor is software that creates and runs virtual machines. VirtualBox is a Type 2 hypervisor, meaning it runs on top of your host operating system.

**Q: Why do we use Virtual Machines instead of physical servers for labs?**
A: VMs allow us to safely test configurations, break things, and roll back using snapshots without risking production hardware or spending money on physical servers.

<img width="1366" height="727" alt="Server-installed-on-VMware" src="https://github.com/user-attachments/assets/3b177559-d423-4c0a-9c37-3377c25e4156" />

