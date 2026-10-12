# Day 17 — Subnet Calculators & Route Commands

## Key Concepts

A routing table is a device's address book for destinations — every entry says "to reach X, send through Y." The most important entry is the default route, the catch-all for any destination without a specific match. Windows shows it with "route print", Linux with "ip route", and Cisco routers with "show ip route". Subnet calculators are useful for verification, but hand-calculation is required for the CCNA exam and for understanding network design.

## Lab

### 1. Windows route print
Ran "route print" on my laptop and identified the key entries:
- Default route (0.0.0.0 → 192.168.0.1) — the catch-all for internet traffic
- Loopback (127.0.0.1) — testing the network stack
- Local subnet (192.168.0.0/24) — directly reachable, no router needed
- APIPA entries (169.254.x.x) — for an unused adapter with no DHCP

### 2. Cisco show ip route
Ran "show ip route" on R1 from the Day 16 topology. Output showed:
- 4 connected (C) routes — one per subnet (/26, /27, /28, /30)
- 4 local (L) routes — R1's own IP on each interface (/32 host routes)
- "Gateway of last resort is not set" — R1 has no default route

### 3. Subnet calculator verification
Verified 2 Day 16 answers:
- 192.168.10.0/26 → network .0, usable .1–.62, broadcast .63 ✓
- 192.168.10.64/27 → network .64, usable .65–.94, broadcast .95 ✓

## Why It Matters

When a device can reach some networks but not others, the routing table tells you immediately if a route is missing. This is a core L1/L2 troubleshooting step — check the routing table before assuming a cable or hardware issue.

## Interview Q&A

**Q: Why learn to subnet by hand if calculators exist?**
A: The CCNA exam doesn't allow a calculator, and understanding the math lets you reason about network design instead of just accepting a tool's output.

**Q: What does the route print / ip route command show?**
A: The device's routing table — which networks it knows how to reach and through which gateway or interface.

**Q: What is a default route?**
A: The catch-all entry — traffic for any destination without a specific route gets sent to the default gateway. This is how devices reach the internet.


<img width="623" height="382" alt="day17-route-print" src="https://github.com/user-attachments/assets/049cf8f3-4b80-405a-8852-1dfab39b5134" />

<img width="1132" height="666" alt="day-17-show-ip-route-R1" src="https://github.com/user-attachments/assets/17736b19-40ee-451e-b3a2-19416ef09054" />

<img width="772" height="528" alt="day-17-subnet-calculator-verify" src="https://github.com/user-attachments/assets/1973b1d8-095a-495f-93e8-b6432abb0cbe" />




[SCREENSHOT: route print output]
[SCREENSHOT: R1 show ip route]
[SCREENSHOT: Subnet calculator verification]
