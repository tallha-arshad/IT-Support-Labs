# Day 6 — Week 1 Review — Mapping a Home Network to the OSI Model

## Key Concepts

Consolidation day applying Days 1–5 to a real network: documenting router, devices, and connection types the way a technician would, layer by layer.

## Lab

Ran `ipconfig /all` on my home laptop to identify my own network configuration:
- Physical Address (MAC) — Layer 2
- IPv4 Address, Subnet Mask, Default Gateway — Layer 3
- DNS Servers — Layer 7

Ran `tracert google.com` to trace the path from my laptop to Google's servers:
- Hop 1 — my own router (Layer 3)
- Hops 2+ — ISP and beyond

<img width="709" height="727" alt="day06-ipconfig-all" src="https://github.com/user-attachments/assets/6e1882a8-caf4-4e07-8abc-7a84620f8bd9" />

<img width="666" height="458" alt="day06-tracert" src="https://github.com/user-attachments/assets/dbe19a8b-949b-4eb7-9ac5-d3e8716b28f2" />


## Why It Matters

Being able to walk through your own network layer-by-layer is a common informal L1 interview exercise ("walk me through what happens when you open a browser").

## Interview Q&A

**Q: Why is a bottom-up (physical-first) troubleshooting approach preferred?**
A: Physical issues are the most common root cause and fastest to rule out — checking a cable takes seconds versus wasting an hour chasing the wrong layer.

**Q: What OSI layer does a switch operate at?**
A: Layer 2 (Data Link) — switches forward traffic based on MAC addresses within the same local network.

**Q: What does an APIPA address (169.254.x.x) tell you?**
A: That the device failed to get an IP from DHCP and self-assigned one. It's a Layer 3 symptom caused by a Layer 1/2 problem — no DHCP server reachable.

## Week 1 Summary

- Day 1: Computer hardware — CPU, RAM, storage, motherboard, PSU
- Day 2: LAN, WAN, MAN — network types by geographic scope
- Day 3: Client-server model and how the internet works
- Day 4: OSI Model Layers 1–3 — physical, data link, network
- Day 5: OSI Model Layers 4–7 — transport, session, presentation, application
- Day 6: Mapped my own network to the OSI model
