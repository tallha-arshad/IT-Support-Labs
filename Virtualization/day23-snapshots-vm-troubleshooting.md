# Day 23 - Snapshots & Basic VM Troubleshooting

## Key Concepts
A Snapshot saves the exact state of a Virtual Machine at a specific moment. If you make a mistake, you can instantly roll back. This is essential for IT labs, allowing you to safely test risky configurations or updates. Snapshots are taken from the Hypervisor (VirtualBox/VMware), not inside Windows Server Manager.

## Lab
- In VirtualBox, clicked the "Snapshots" menu and took a snapshot of the VM named "Clean Install - Before Changes".
- Intentionally broke the configuration inside Windows Server by changing the static IP to an invalid address (e.g., 10.0.0.99).
- Restarted the VM and verified network connectivity was broken.
- In VirtualBox, opened the Snapshot Manager and restored the VM back to the "Clean Install" state.
- Verified the VM was back online with the correct IP address (192.168.1.10).

## Why It Matters
In production, servers are often snapshotted (or backed up) before major patches. If the patch breaks the system, reverting takes minutes instead of hours of troubleshooting.

## Interview Q&A

**Q: Why take a snapshot before making a major change?**
A: Because even careful changes can cause unexpected issues. A snapshot provides a guaranteed, instant rollback if the change breaks the server, minimizing downtime.

<img width="1366" height="730" alt="Server-Snapshot" src="https://github.com/user-attachments/assets/b8a5a21d-605a-430b-a437-832920145574" />

<img width="1366" height="707" alt="Restoring from Snapshot" src="https://github.com/user-attachments/assets/a05a566f-59a9-4487-a7d3-73a7902dcd03" />
