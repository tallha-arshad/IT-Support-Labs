# Day 8 — IPv4 Address Structure & Classes

## Key Concepts

An IPv4 address is four 8-bit numbers (called octets) separated by dots, giving a total of 32 bits. Example: 192.168.1.10.

Each octet ranges from 0 to 255. Add them together and you get 32 bits (4 × 8 = 32).

Addresses are historically grouped into classes based on the first octet, which determines the default network size:

- Class A: 1 to 126 (first bit 0)
- Class B: 128 to 191 (first two bits 10)
- Class C: 192 to 223 (first three bits 110)
- Class D: 224 to 239 (multicast, not used for hosts)
- Class E: 240 to 255 (reserved, experimental)

Special addresses:
- 127.0.0.0 to 127.255.255.255 — loopback. 127.0.0.1 is "localhost," meaning this machine itself.
- 169.254.x.x — APIPA. Self-assigned when DHCP fails.
- 0.0.0.0 — unspecified address, used by a device before it has a real IP.

## Lab

Classified the following IP addresses by class:

- 10.0.0.5 → Class A (first octet 10, within 1-126)
- 172.16.5.1 → Class B (first octet 172, within 128-191)
- 192.168.1.1 → Class C (first octet 192, within 192-223)
- 8.8.8.8 → Class A (first octet 8)
- 127.0.0.1 → Loopback, not a class
- 169.254.10.5 → APIPA, not a class

Ran `ipconfig /all` on my laptop and identified:
- My IPv4 address
- My subnet mask
- My default gateway

The IP address I use at home falls in the Class C private range (192.168.x.x), which is what most home routers use.

Wrote down the usable host range for a default Class C network:
- Network: 192.168.x.0
- Usable hosts: 192.168.x.1 to 192.168.x.254
- Broadcast: 192.168.x.255
- Total usable: 254 addresses

## Why It Matters

When a user reads their IP over the phone, you can instantly tell:

- Is this a normal Class C home address? (192.168.x.x)
- Did they misread it? (something outside 0-255 per octet)
- Is it a loopback? (127.x.x.x)
- Is DHCP broken? (169.254.x.x)

That recognition saves time on every call.

## Interview Q&A

**Q: What class is 10.0.0.5, and how do you know?**
A: Class A. The first octet is 10, which falls in the Class A range (1-126). Class A is used for very large networks.

**Q: A user reads you the IP 169.254.10.5. What does that tell you immediately?**
A: That's an APIPA address, meaning the device failed to get an IP from DHCP and self-assigned one. The actual problem is a DHCP failure, not whatever the user was originally trying to do.

**Q: What is 127.0.0.1 used for?**
A: It's the loopback address. It refers to the machine itself and is used to test whether the network stack is working. It never identifies a device on a real network.

**Q: How many octets are in an IPv4 address, and how many bits total?**
A: Four octets, 32 bits total. Each octet is 8 bits and ranges from 0 to 255.

**Q: What's the difference between a network address, a broadcast address, and a usable host address?**
A: The network address (first address in the range) identifies the network itself. The broadcast address (last address) sends data to all devices on the network. Every address between them is a usable host address. For a Class C network, that's 254 usable addresses.


