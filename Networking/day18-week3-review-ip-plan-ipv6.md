# Day 18 — Week 3 Review: IP Plan Design & IPv6 Basics

## Key Concepts

Week 3 consolidation: applying VLSM to design a complete IP plan for a small office. Also introduced IPv6 — a 128-bit address (vs IPv4's 32-bit), written in 8 groups of hexadecimal separated by colons, with abbreviation rules for leading zeros and consecutive zero groups.

## Lab

### IP Plan Design — 10.10.0.0/22

Designed a full IP plan for a fictional office using VLSM:

| Dept | Hosts | CIDR | Network | Usable Range | Broadcast |
|---|---|---|---|---|---|
| Sales | 200 | /24 | 10.10.0.0 | 10.10.0.1 – 10.10.0.254 | 10.10.0.255 |
| HR | 100 | /25 | 10.10.1.0 | 10.10.1.1 – 10.10.1.126 | 10.10.1.127 |
| IT | 50 | /26 | 10.10.1.128 | 10.10.1.129 – 10.10.1.190 | 10.10.1.191 |
| Mgmt | 10 | /28 | 10.10.1.192 | 10.10.1.193 – 10.10.1.206 | 10.10.1.207 |
| Network | 5 | /29 | 10.10.1.208 | 10.10.1.209 – 10.10.1.214 | 10.10.1.215 |

Remaining space: 10.10.1.216 – 10.10.3.255 (for future growth)

### IPv6 Abbreviation Practice

Abbreviated 3 full IPv6 addresses:
- 2001:0db8:0000:0000:0000:ff00:0042:8329 → 2001:db8::ff00:42:8329
- fe80:0000:0000:0000:0202:b3ff:fe1e:8329 → fe80::202:b3ff:fe1e:8329
- 0000:0000:0000:0000:0000:0000:0000:0001 → ::1

## Why It Matters

Designing an IP plan from scratch proves you understand subnetting, not just formulas. IPv6 knowledge is tested on CCNA and increasingly required in real networks running dual-stack.

## Interview Q&A

**Q: Walk me through designing an IP plan for a new office.**
A: List departments and host counts, choose a private range with room to grow, use VLSM to size each subnet, reserve a small subnet for network equipment, and document everything in a table before implementing.

**Q: Why does a single subnet in IPv6 almost always use /64?**
A: Because IPv6's address space is enormous, /64 provides plenty of addresses while leaving room for subnetting and SLAAC autoconfiguration.

**Q: What does the "::" mean in an IPv6 address?**
A: It represents one run of consecutive all-zero groups. Only one "::" is allowed per address.
