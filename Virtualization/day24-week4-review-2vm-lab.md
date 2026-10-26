# Day 24 - Week 4 Review Lab — Building a 2-VM Lab Environment

## Key Concepts
A single server isn't enough to practice IT. You need a "Client" VM to test how a real user connects to the server. This week's review is building a 2-VM environment (Server + Client) on the same virtual network. This is the foundational setup required before we install Active Directory in Week 5.

## Lab
- Created a second Virtual Machine in VirtualBox and installed Windows 10/11 (the Client VM).
- Configured the Network Adapter for both the Server VM (DC01) and the Client VM to use the same "Internal Network" (or Host-Only adapter) so they can communicate without interfering with the host internet.
- Assigned the Client VM a static IP address in the same subnet as the server (Server: 192.168.1.10, Client: 192.168.1.20).
- Set the Server's IP (192.168.1.10) as the Default Gateway on the Client VM.
- Opened Command Prompt on the Client VM and successfully pinged the Server (`ping 192.168.1.10`).
- Took a snapshot of both VMs labeled "Ready for Active Directory".

## Why It Matters
Real IT environments involve servers providing services and clients consuming them. This two-VM setup is exactly what we need to practice Active Directory, DNS, and Group Policy in the upcoming weeks.

## Interview Q&A

**Q: Your Client VM cannot ping the Server VM. What is the first thing you check?**
A: I would check the network settings of both VMs to ensure they are on the same virtual network (like Internal Network) and verify their IP addresses are in the same subnet. I would also check if the Windows Firewall on the Server is blocking ICMP (ping) requests.


<img width="1366" height="729" alt="Both-machines-running" src="https://github.com/user-attachments/assets/3caf51ac-c9cc-44c9-bdd7-887c28daa346" />
