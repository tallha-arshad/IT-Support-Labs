# IT Support Labs

Hands-on labs from my IT Support / Networking training. Built with Cisco Packet Tracer, VMware, Windows Server, Active Directory, and Microsoft 365.

## About This Repository

I'm working through a structured IT Support program designed around one goal: landing a Helpdesk L1 / IT Support role.

The path is staged:

1. Foundation (Days 1-30): networking, subnetting, Windows Server, Active Directory.
2. L1-Critical (Days 31-54): the skills actually tested in L1 interviews and used daily in L1 jobs.
3. AZ-900 Prep (Days 55-60): Microsoft Azure Fundamentals certification.
4. Deeper Learning (Days 61+): CCNA networking, deep DNS/DHCP, Group Policy, DevOps - pursued while employed.

Every day I study the theory, do a hands-on lab, and document it here with screenshots as proof.

## Current Progress

| Phase | Days | Topics | Status |
|---|---|---|---|
| Foundation | 1-6 | Computer hardware, LAN/WAN/MAN, client-server, OSI model | Done |
| Foundation | 7-12 | Binary, IPv4, subnetting, ipconfig, ping, nslookup | Done |
| Foundation | 13-18 | Subnet masks, CIDR, VLSM, route commands, IPv6 basics | Done |
| Foundation | 19-24 | VirtualBox, Windows Server setup, VM networking, snapshots | Done |
| Foundation | 25-30 | Active Directory - DC promotion, OUs, users, groups, PowerShell | Done |
| L1-Critical | 31-36 | Microsoft 365, Entra ID, Intune, Exchange Online, Security, Onboarding | In progress |
| L1-Critical | 37-42 | Windows troubleshooting, BSOD, BIOS/UEFI, printers, hardware faults | Coming |
| L1-Critical | 43-48 | Real tickets + Incident Response + STAR interview prep | Coming |
| L1-Critical | 49-54 | Windows CMD, PowerShell, Linux basics | Coming |
| AZ-900 Prep | 55-60 | Microsoft Azure Fundamentals exam preparation | Coming |
| Deeper Learning | 61+ | CCNA deep dive, deep DNS/DHCP, deep Group Policy, DevOps | Later |

## Full Day-by-Day Lab Index

Click any day to jump straight into that specific lab file.

### Phase 1: Foundation (Days 1-30)

**Fundamentals**
- [Day 1 - Computer Hardware](./Fundamentals/day01-computer-hardware.md)
- [Day 2 - LAN, WAN, MAN](./Fundamentals/day02-lan-wan-man.md)
- [Day 3 - Client-Server Model](./Fundamentals/day03-client-server-model.md)
- [Day 4 - OSI Layers 1-3](./Fundamentals/day04-osi-layers-1-3.md)
- [Day 5 - OSI Layers 4-7](./Fundamentals/day05-osi-layers-4-7.md)
- [Day 6 - Week 1 Review (OSI Mapping)](./Fundamentals/day06-week1-review-osi-mapping.md)

**Networking**
- [Day 7 - Binary Number System](./Networking/day07-binary-number-system.md)
- [Day 8 - IPv4 Structure & Classes](./Networking/day08-ipv4-structure-classes.md)
- [Day 9 - Private vs Public IPs & NAT](./Networking/day09-private-public-nat.md)
- [Day 10 - ipconfig Network Config](./Networking/day10-ipconfig-network-config.md)
- [Day 11 - ping, nslookup](./Networking/day11-ping-nslookup.md)
- [Day 12 - Week 2 Review (No Internet Ticket)](./Networking/day12-week2-review-no-internet-ticket.md)
- [Day 13 - Subnet Mask & CIDR](./Networking/day13-subnet-mask-cidr.md)
- [Day 14 - Subnetting Formula](./Networking/day14-subnetting-formula.md)
- [Day 15 - Splitting a /24 into 4 Subnets](./Networking/day15-splitting-24-into-4-subnets.md)
- [Day 16 - VLSM (Unequal-Sized Subnets)](./Networking/day16-vlsm-unequal-subnets.md)
- [Day 17 - Subnet Calculators & Route Commands](./Networking/day17-subnet-calculators-route-commands.md)
- [Day 18 - IP Plan Design & IPv6](./Networking/day18-week3-review-ip-plan-ipv6.md)

**Virtualization**
- [Day 19 - VirtualBox & First VM](./Virtualization/day19-installing-virtualbox-first-vm.md)
- [Day 20 - VM Networking Modes](./Virtualization/day20-vm-networking-modes.md)
- [Day 21 - Installing Windows Server](./Virtualization/day21-installing-windows-server.md)
- [Day 22 - Initial Server Configuration](./Virtualization/day22-initial-server-config.md)
- [Day 23 - Snapshots & VM Troubleshooting](./Virtualization/day23-snapshots-vm-troubleshooting.md)
- [Day 24 - Week 4 Review (2-VM Lab)](./Virtualization/day24-week4-review-2vm-lab.md)

**Active Directory**
- [Day 25 - What is Active Directory](./ActiveDirectory/day25-what-is-active-directory.md)
- [Day 26 - Promoting a DC](./ActiveDirectory/day26-promoting-domain-controller.md)
- [Day 27 - Organizational Units](./ActiveDirectory/day27-organizational-units.md)
- [Day 28 - Creating Users & Groups](./ActiveDirectory/day28-creating-users-groups.md)
- [Day 29 - AD PowerShell Cmdlets](./ActiveDirectory/day29-ad-powershell-cmdlets.md)
- [Day 30 - Week 5 Review (AD Structure)](./ActiveDirectory/day30-week5-review-ad-structure.md)

### Phase 2: L1-Critical (Days 31-54)

**Microsoft 365 & Cloud Identity**
- [Day 31 - M365 Tenant Setup & Admin Center](./Microsoft365/day31-m365-tenant-setup.md)
- [Day 32 - User Onboarding & Licensing](./Microsoft365/day32-m365-user-onboarding.md)
- [Day 33 - Password Reset & Offboarding](./Microsoft365/day33-m365-helpdesk-offboarding.md)
- [Day 34 - Microsoft Entra ID & Sign-in Logs](./Microsoft365/day34-microsoft-entra-id.md)
- Day 35 - Exchange Online (In progress)
- Day 36 - Security & Onboarding (Coming)
- Day 37-42 - Windows & Hardware Troubleshooting (Coming)
- Day 43-48 - Real Tickets & Interview Prep (Coming)
- Day 49-54 - Command Line Basics (Coming)

## Tools and Technologies

- Cisco Packet Tracer
- VMware Workstation
- Windows Server 2019/2022
- Windows 10/11
- Active Directory Domain Services
- Microsoft 365 (Admin Center, Entra ID, Exchange Online)
- PowerShell
- Windows CMD

## Format of Each Day File

Each day's markdown file follows a consistent structure:

- Key Concepts: what the topic is and why it matters
- Lab: what I built, configured, or tested
- Why It Matters: real-world relevance and exam relevance
- Interview Q&A: common questions on that topic with answers
- Screenshots: proof of the actual work

## Connect

- LinkedIn: linkedin.com/in/tallha-arshad
- Email: tallha383@gmail.com

Currently looking for an IT Support / Helpdesk L1 role. Open to relocation.

#ITSupport #Networking #ActiveDirectory #WindowsServer #M365 #EntraID #LearningInPublic
