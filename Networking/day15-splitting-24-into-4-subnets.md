# Day 15 — Splitting a /24 Into 4 Equal Subnets

## Key Concepts
Splitting a network into N equal subnets requires borrowing enough bits so that
2^(borrowed bits) >= N. Splitting 192.168.1.0/24 into 4 equal subnets means
borrowing 2 bits (2^2 = 4), turning it into four /26 networks, each with 62
usable hosts. The block size (step between subnets) for a /24 split into 4 is
256 / 4 = 64.

## Lab
Expanded the router from Day 14 by installing two WIC-1ENET modules, giving it
4 total interfaces instead of 2, one per subnet:
- Street 1: 192.168.1.0/26 — router Fa0/0: .1, PC0: .2
- Street 2: 192.168.1.64/26 — router Fa0/1: .65, PC1: .66
- Street 3: 192.168.1.128/26 — router Eth0/0/0: .129, PC2: .130
- Street 4: 192.168.1.192/26 — router Eth0/1/0: .193, PC3: .194

Verified all 4 interfaces up/up via `show ip interface brief`, then confirmed
full connectivity with zero packet loss pinging between all 4 PCs across the router.

## Why It Matters
"Split this block evenly across N departments" is one of the most common real
subnetting tasks and CCNA exam question types, and also demonstrates a key
trade-off: subnetting costs usable addresses (4 x 62 = 248 vs. 254 if left
as one flat /24), since each new subnet needs its own network and broadcast address.

## Interview Q&A
**Q: You need to split a /24 into 4 equal subnets. What's the new CIDR?**
/26 — splitting into 4 equal parts means borrowing 2 bits (2^2 = 4), which
turns a /24 into four /26 subnets, each with 62 usable hosts.

**Q: Why does subnetting reduce the total number of usable addresses?**
Every subnet needs its own network address and broadcast address, which can't
be assigned to devices. Splitting a /24 into 4 subnets costs 6 addresses
total (2 per subnet x 4) compared to leaving it as one flat network.

<img width="1105" height="768" alt="slash 24 into 4 Equal Subnets" src="https://github.com/user-attachments/assets/c4c90079-7aee-4501-b2cd-c1a5fc736c64" />
