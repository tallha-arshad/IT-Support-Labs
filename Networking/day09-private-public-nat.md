# Day 9 — Private vs Public IP Ranges & NAT Concept

## Key Concepts

Private IP ranges are reserved for internal networks and never routed on the public internet. There are three:

- 10.0.0.0 to 10.255.255.255 (10.0.0.0/8)
- 172.16.0.0 to 172.31.255.255 (172.16.0.0/12)
- 192.168.0.0 to 192.168.255.255 (192.168.0.0/16)

Public IP addresses are assigned by an ISP and are routable on the internet. Because there aren't enough public IPs for every device in the world, NAT (Network Address Translation) on the router translates many private internal addresses into one shared public address.

This is why your laptop shows 192.168.x.x in ipconfig, but whatismyip.com shows a completely different address. Both are your IP, at different layers of the connection.

## Lab

Ran ipconfig on my laptop and noted my private IP. Then visited a "what is my IP" site and noted my public IP. Confirmed they are different.

Private IP: 192.168.x.x (assigned by my home router via DHCP)
Public IP: shown by the website (assigned by my ISP, shared via NAT)

Classified addresses as private or public:

- 192.168.0.1 → Private (Class C private range)
- 8.8.8.8 → Public (Google DNS)
- 172.20.10.5 → Private (172.16-31.x.x range)
- 1.1.1.1 → Public (Cloudflare DNS)
- 10.0.0.5 → Private (Class A private range)
- 172.32.0.1 → Public (outside the 172.16-31 private range)

Memorized the three private ranges:

- 10.x.x.x — Class A private
- 172.16.x.x to 172.31.x.x — Class B private (only 16 to 31, not the whole 172 range)
- 192.168.x.x — Class C private

## Why It Matters

Every ticket involving a user's IP address touches NAT:

- "My IP is 192.168.1.5" — that's the private IP, use ipconfig to see it
- "But whatismyip says my IP is 203.0.113.45" — that's the public IP after NAT
- "My security camera isn't reachable from outside" — port forwarding, a NAT-related task
- "My public IP changed" — most home ISPs assign dynamic public IPs, not static ones

Understanding NAT avoids confusion on calls and lets you explain it to users simply.

## Interview Q&A

**Q: Explain what NAT does in one sentence.**
A: NAT translates many private internal IP addresses into one shared public IP address so an entire office or home can share a single internet connection.

**Q: Why does a user's "my IP" from a website not match their ipconfig output?**
A: Because ipconfig shows the private internal IP, while the website shows the public IP after NAT translation on the router. They're two different addresses for two different purposes, not a bug.

**Q: What are the three private IP ranges?**
A: 10.0.0.0/8, 172.16.0.0/12 (172.16 through 172.31), and 192.168.0.0/16.

**Q: What is port forwarding used for?**
A: It lets external traffic reach a specific device inside a private network — for example, a home security camera or a game server that needs to be reachable from the internet.

**Q: Why don't private IPs work on the internet?**
A: They're reserved by design and routers on the public internet refuse to route them. Only public IPs are routable on the internet. NAT bridges the two.

<img width="830" height="768" alt="ipconfigall" src="https://github.com/user-attachments/assets/e3faa651-9089-4a3c-9fc6-5818f74bd3a1" />


<img width="771" height="329" alt="MyIP" src="https://github.com/user-attachments/assets/02cf84ae-ba67-43b2-b274-df89e5303325" />
