# Day 16 — VLSM (Unequal-Sized Subnets)

## Key Concepts

VLSM (Variable Length Subnet Masking) allows subnets of different sizes to be carved from the same block. Rule: sort subnets largest to smallest, allocate largest first, ensure no overlap, use /30 for router-to-router links.

## Lab

Built a VLSM topology in Packet Tracer using 192.168.10.0/24:

- Sales: /26 — 192.168.10.0/26 — hosts .1–.62 — broadcast .63
- HR: /27 — 192.168.10.64/27 — hosts .65–.94 — broadcast .95
- IT: /28 — 192.168.10.96/28 — hosts .97–.110 — broadcast .111
- Router Link: /30 — 192.168.10.112/30 — hosts .113–.114 — broadcast .115

Configured Router1 with 3 subinterfaces (dot1Q 26/27/28) plus a serial link to Router2. Configured Switch0 with VLANs 26/27/28 on access ports and a trunk on Fa0/4. Static route on R2 to reach all subnets.

Verified with:
- show ip interface brief (all up/up)
- show ip route (all subnets present)
- Ping from PC-Sales to all other gateways and R2's link IP
- All pings successful with 0% packet loss

## Why It Matters

VLSM is how real networks are designed — matching subnet size to actual need. Core CCNA topic and real interview question.

## Interview Q&A

**Q: What is VLSM and why use it instead of equal subnetting?**
A: VLSM lets you carve subnets of different sizes from one block, matching each subnet to its actual need. Far more address-efficient than equal-sized blocks.

**Q: Why does a router-to-router link only need a /30 subnet?**
A: A /30 gives exactly 2 usable addresses — all a point-to-point link needs. Anything bigger wastes address space.

<img width="816" height="584" alt="1-Full Topology" src="https://github.com/user-attachments/assets/a8c164b1-628d-4482-a3a0-abf8b7b1e46d" />
<img width="1145" height="641" alt="2-R1CLI" src="https://github.com/user-attachments/assets/28990021-7760-4748-adab-df3f1fef09a2" />
<img width="1015" height="693" alt="3-R1CLI" src="https://github.com/user-attachments/assets/aab9e023-c4ce-4a57-adf3-9c3ed5124225" />
<img width="1163" height="701" alt="PC Sales Command -1" src="https://github.com/user-attachments/assets/1e655e26-84df-4bc9-a2bb-f40f8fc1f19b" />
<img width="1167" height="704" alt="PC Sales Command-2" src="https://github.com/user-attachments/assets/7b381dc1-e648-436b-9a2d-4159d959c585" />



