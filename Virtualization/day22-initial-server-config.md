# Day 22 - Initial Server Configuration (Server Manager, Roles & Features)

## Key Concepts
Server Manager is the main dashboard for Windows Server. "Roles" are major functions a server provides (like AD DS, DNS, DHCP), while "Features" are supporting tools. Before adding roles, a server should have a Static IP so clients can always find it.

## Lab
- Opened Server Manager and reviewed the dashboard.
- Changed the server's hostname to "DC01" via Local Server and restarted the server.
- Set a Static IP address: In Server Manager > Local Server, clicked the "Ethernet" link. Right-clicked the adapter > Properties > IPv4 > set IP to 192.168.1.10 and Subnet to 255.255.255.0.
- Opened the "Add Roles and Features" wizard and explored the list of available roles.
- Confirmed the difference between a Server Role and a Feature.

## Why It Matters
Servers must have predictable IP addresses. If a Domain Controller's IP changes, all the client PCs will lose their connection to Active Directory.

## Interview Q&A

**Q: Why must a server have a static IP address?**
A: Servers provide services (like DNS or file sharing) to clients. If their IP address changed via DHCP, clients wouldn't know where to find those services, causing network outages.

<img width="1366" height="655" alt="Server-StaticIP" src="https://github.com/user-attachments/assets/a3ba5407-1f63-4dc9-ae68-e4ccb5f6d075" />
