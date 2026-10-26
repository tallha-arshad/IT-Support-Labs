# Day 20 - VM Networking Modes (NAT, Bridged, Host-Only)

## Key Concepts
When you create a VM, you must choose how it connects to the network. VirtualBox offers three main modes: 
1. **NAT:** The VM gets internet access through the host's connection but is hidden from the rest of the local network. 
2. **Bridged:** The VM appears as its own separate device on the physical LAN with its own IP.
3. **Host-Only:** The VM can only talk to the host machine, with no internet access.

## Lab
- Set the VM network adapter to NAT and verified it could reach the internet.
- Switched the adapter to Bridged mode and verified it pulled an IP address from the physical home router.
- Switched to Host-Only mode and confirmed the VM could ping the host machine but not the internet.
- Left the configuration on NAT for future lab isolation.

## Why It Matters
Choosing the wrong network mode is the #1 reason beginners can't get their VMs to talk to each other or the internet. Understanding NAT vs Bridged is critical for setting up Active Directory labs.

## Interview Q&A

**Q: What is the difference between NAT and Bridged networking in a VM?**
A: NAT hides the VM behind the host's IP address, allowing it internet access but preventing other devices from reaching it. Bridged mode gives the VM its own IP address on the physical network, making it visible to other devices on the LAN.

<img width="1366" height="728" alt="Network-modes-On-VMware-machine" src="https://github.com/user-attachments/assets/030f8543-a8e6-4b1e-8211-3b3e78fa0313" />
