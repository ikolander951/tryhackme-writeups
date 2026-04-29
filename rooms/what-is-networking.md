# What is Networking?

**Path:** Pre-Security / Networking foundations
**Difficulty:** Info / Easy
**Date completed:** 2026-04 (revisit and confirm)
**Room link:** https://tryhackme.com/room/whatisnetworking

---

## What this room teaches

A bite-sized tour of how computers talk to each other: what a network is, how devices identify themselves with IP and MAC addresses, and the basic protocols that move data from point A to point B. It's the room you do before anything else makes sense.

## Key takeaways

- A **network** is two or more devices connected so they can share data. Networks scale from a home Wi-Fi router to the public internet.
- Every device on a network needs a unique address. **IP addresses** identify devices on the network layer (and can change). **MAC addresses** identify the physical hardware (burned in, doesn't change).
- **Ping** is the simplest connectivity test — it sends an ICMP echo request and waits for a reply. If a host answers, it's reachable. If it doesn't, either the host is down, blocked by a firewall, or somewhere in between is dropping the packets.

## What was new to me

- The fact that an IP address is reassignable but a MAC is fixed to the hardware. That distinction matters later when you're tracking a device that moves between networks (DHCP changes the IP; the MAC stays the same).
- Ping isn't always reliable as a "host is alive" signal — many production servers block ICMP. Absence of a ping reply doesn't prove the host is offline.

## How a SOC analyst would use this

- **Triaging a network alert** starts with knowing what the source and destination IPs represent. Internal IP? External? Is the asset in our CMDB? Without networking fundamentals, that question doesn't make sense.
- **Lateral movement detection** depends on understanding that an attacker who's compromised one host will pivot to others using IPs and ports — so seeing unusual outbound connections from a workstation to other workstations is a flag worth investigating.
- **Phishing investigations** routinely involve resolving a suspicious domain to an IP, then checking who else in the org communicated with that IP. Day-one SOC work.

## Commands / concepts to remember

| Concept | What it is |
|---------|------------|
| IP address | Logical, network-layer address for a device |
| MAC address | Physical hardware address (12 hex chars) |
| `ping <host>` | ICMP echo test for basic reachability |
| Public vs private IP | Public = routable on the internet; private = inside a LAN (10.x, 172.16-31.x, 192.168.x) |

## Resources

- Room: https://tryhackme.com/room/whatisnetworking
- Related: Networking Concepts (next on my Cyber Security 101 path)
