# CCNA 200-301 Study Guide

**16-Week Plan · ~5–6 Hours/Week**

> Resources used throughout: 📘 Cisco Cert Guide · 🎥 Jeremy's IT Lab · 🖥️ Packet Tracer · 📅 31 Days Before Your CCNA

---

## Exam Quick Reference

| Detail | Info |
|--------|------|
| Exam Code | 200-301 |
| Duration | 120 minutes |
| Questions | ~100 |
| Passing Score | 825 / 1000 |
| Format | MCQ + Sim/Simlet |
| Valid For | 3 Years |

---

## Progress Tracker

| Week | Topic                                       | Done |
| ---- | ------------------------------------------- | ---- |
| 1    | Networking Fundamentals & OSI Model         | ☐    |
| 2    | Ethernet, Switching & VLANs Pt. 1           | ☐    |
| 3    | VLANs Pt. 2, Trunking & STP                 | ☐    |
| 4    | IPv4 Addressing & Subnetting                | ☐    |
| 5    | IPv4 Routing Fundamentals                   | ☐    |
| 6    | OSPF Single-Area                            | ☐    |
| 7    | Inter-VLAN Routing & EtherChannel           | ☐    |
| 8    | ACLs & NAT                                  | ☐    |
| 9    | DHCP, DNS & NTP                             | ☐    |
| 10   | Device Security & Management                | ☐    |
| 11   | Wireless & Network Security Concepts        | ☐    |
| 12   | IPv6 Addressing & Routing                   | ☐    |
| 13   | Automation, SDN & Network Programmability   | ☐    |
| 14   | Full Review — Routing & Switching Deep Dive | ☐    |
| 15   | Full Review — Security, WAN & IPv6          | ☐    |
| 16   | Exam Simulation & Final Polish              | ☐    |

---

## Phase 1 — Foundation (Weeks 1–3)

---

### Week 1 · Networking Fundamentals & OSI Model
**~5.5 hours**

**Topics**
- OSI & TCP/IP Models
- Network Topologies
- Ethernet & LAN Basics
- Binary/Hex Math

**Resources**
- 📘 Cisco Cert Guide Ch. 1–2 — Networking Models & Fundamentals
- 🎥 Jeremy's IT Lab: Day 1–3 — Networking Models (OSI & TCP/IP)
- 🖥️ Packet Tracer: Build a simple LAN — PCs, switch, observe frames
- 📅 31 Days: Day 31 — Networking Models review

**Lab**
Connect 3 PCs to a switch. Use Simulation mode to watch ARP and ping traffic at each OSI layer.

**Exam Tip**
Memorize the OSI layers top-down AND bottom-up. Use: *"All People Seem To Need Data Processing"* and reverse.

---

### Week 2 · Ethernet, Switching & VLANs Pt. 1
**~5.5 hours**

**Topics**
- MAC Addresses & Ethernet Frames
- Switch Operation & MAC Tables
- Half/Full Duplex
- Intro to VLANs

**Resources**
- 📘 Cisco Cert Guide Ch. 3–5 — LAN Switching
- 🎥 Jeremy's IT Lab: Day 4–8 — Ethernet, Interfaces, VLANs
- 🖥️ Packet Tracer: Configure VLANs on a 2960 switch, verify with `show vlan brief`
- 📅 31 Days: Day 30 — LAN Switching

**Lab**
Create 3 VLANs (10, 20, 30). Assign ports. Verify PCs in the same VLAN can ping; different VLANs cannot.

**Exam Tip**
Run `show mac address-table` repeatedly after pings to watch it populate. Understanding this is crucial for the exam.

---

### Week 3 · VLANs Pt. 2, Trunking & STP
**~5.5 hours**

**Topics**
- 802.1Q Trunking
- DTP
- Spanning Tree Protocol (STP)
- PortFast & BPDU Guard

**Resources**
- 📘 Cisco Cert Guide Ch. 6–8 — VLANs, Trunking, STP
- 🎥 Jeremy's IT Lab: Day 9–11 — Trunking, DTP, STP
- 🖥️ Packet Tracer: Configure trunk links, verify STP root bridge election
- 📅 31 Days: Day 29 — VLANs & Trunking · Day 28 — STP

**Lab**
Connect 3 switches in a triangle. Identify the root bridge. Manually set root priority. Enable PortFast on access ports.

**Exam Tip**
STP port states: Blocking → Listening → Learning → Forwarding. Draw the triangle topology and label each port state.

---

## Phase 2 — IP Addressing (Weeks 4–5)

---

### Week 4 · IPv4 Addressing & Subnetting ⭐
**~6 hours**

**Topics**
- IPv4 Address Classes
- Subnet Masks & CIDR
- Subnetting Practice
- VLSM

**Resources**
- 📘 Cisco Cert Guide Ch. 11–13 — IP Addressing & Subnetting
- 🎥 Jeremy's IT Lab: Day 15–18 — Subnetting (Parts 1–4)
- 🖥️ Packet Tracer: Assign correct subnets across a multi-router topology
- 📅 31 Days: Day 23 — IPv4 Addressing

**Lab**
Given `192.168.1.0/24`, create 4 subnets. Assign IPs to routers and PCs. Verify with `show ip interface brief`.

**Exam Tip**
Subnetting is the #1 CCNA skill. Spend extra time here. Practice 10 random subnetting problems daily this week.

---

### Week 5 · IPv4 Routing Fundamentals
**~5.5 hours**

**Topics**
- Routing Concepts
- Static Routes
- Default Routes
- Routing Table Lookup

**Resources**
- 📘 Cisco Cert Guide Ch. 14–15 — IP Routing
- 🎥 Jeremy's IT Lab: Day 19–21 — Static Routing
- 🖥️ Packet Tracer: Configure static routes between 3 routers — full mesh reachability
- 📅 31 Days: Day 22 — IP Routing

**Lab**
Build a 3-router topology. Use static + default routes so all PCs can reach all others. Test with extended ping.

**Exam Tip**
Always check routing tables with `show ip route` and trace the path. Understand Administrative Distance vs. metric.

---

## Phase 3 — Routing Protocols (Weeks 6–7)

---

### Week 6 · OSPF Single-Area
**~5.5 hours**

**Topics**
- OSPF Concepts & LSAs
- Router ID
- Neighbor Adjacencies
- OSPF Configuration

**Resources**
- 📘 Cisco Cert Guide Ch. 18–20 — OSPF
- 🎥 Jeremy's IT Lab: Day 24–27 — OSPF (Parts 1–4)
- 🖥️ Packet Tracer: Configure OSPF Area 0 across 4 routers, verify adjacencies
- 📅 31 Days: Day 20 — OSPF

**Lab**
Configure OSPF on 4 routers. Use `show ip ospf neighbor` and `show ip ospf database` to verify state.

**Exam Tip**
Know the 5 OSPF packet types (Hello, DBD, LSR, LSU, LSAck) and the neighbor state machine for the exam.

---

### Week 7 · Inter-VLAN Routing & EtherChannel
**~5.5 hours**

**Topics**
- Router-on-a-Stick
- Layer 3 Switching / SVIs
- EtherChannel (LACP/PAgP)
- Port Aggregation

**Resources**
- 📘 Cisco Cert Guide Ch. 9–10 — Inter-VLAN Routing, EtherChannel
- 🎥 Jeremy's IT Lab: Day 12–14 — Inter-VLAN Routing, EtherChannel
- 🖥️ Packet Tracer: Configure Router-on-a-Stick for 3 VLANs; then repeat with L3 switch SVIs
- 📅 31 Days: Day 27 — Inter-VLAN Routing

**Lab**
Compare Router-on-a-Stick vs SVI routing. Configure EtherChannel between two switches. Verify with `show etherchannel summary`.

**Exam Tip**
L3 switch SVIs are more scalable than RoaS. Know both configs cold — either can appear on the exam.

---

## Phase 4 — WAN & NAT (Weeks 8–9)

---

### Week 8 · ACLs & NAT
**~5.5 hours**

**Topics**
- Standard ACLs
- Extended ACLs
- Named ACLs
- NAT/PAT Concepts & Config

**Resources**
- 📘 Cisco Cert Guide Ch. 24–26 — ACLs & NAT
- 🎥 Jeremy's IT Lab: Day 34–36 — Standard, Extended & Named ACLs · Day 37 — NAT
- 🖥️ Packet Tracer: Block specific traffic with extended ACL; configure PAT for internet simulation
- 📅 31 Days: Day 16 — ACLs · Day 15 — NAT

**Lab**
Use an extended ACL to block ICMP from one subnet while allowing HTTP. Verify with ping and browser simulation.

**Exam Tip**
Place standard ACLs close to the destination; extended ACLs close to the source. This is an exam favorite.

---

### Week 9 · DHCP, DNS & NTP
**~5 hours**

**Topics**
- DHCP Server & Relay Agent
- DNS Basics
- NTP Configuration
- DHCP Troubleshooting

**Resources**
- 📘 Cisco Cert Guide Ch. 21–22 — DHCP & DNS
- 🎥 Jeremy's IT Lab: Day 38–39 — DHCP, DNS, NTP
- 🖥️ Packet Tracer: Configure a router as DHCP server with a relay agent across subnets
- 📅 31 Days: Day 14 — DHCP

**Lab**
Set up DHCP with excluded ranges. Configure `ip helper-address` for inter-subnet relay. Verify leases with `show ip dhcp binding`.

**Exam Tip**
Know DORA (Discover, Offer, Request, Acknowledge) and why `ip helper-address` is needed across router hops.

---

## Phase 5 — Security & Management (Weeks 10–11)

---

### Week 10 · Device Security & Management
**~5.5 hours**

**Topics**
- Console/SSH/Telnet Security
- Password Encryption
- AAA Concepts
- SNMP, Syslog, NetFlow

**Resources**
- 📘 Cisco Cert Guide Ch. 27–28 — Device Management & Security
- 🎥 Jeremy's IT Lab: Day 40–42 — SSH, CDP/LLDP, NTP, Syslog
- 🖥️ Packet Tracer: Secure a router — disable Telnet, enable SSH v2, configure `login local`
- 📅 31 Days: Day 12 — Management Protocols

**Lab**
Lock down a router: SSH only, exec timeout, encrypted passwords, login banner, privilege levels. Test from a PC.

**Exam Tip**
Know the SSH config sequence cold:
```
hostname → ip domain-name → crypto key generate rsa → ip ssh version 2 → transport input ssh
```

---

### Week 11 · Wireless & Network Security Concepts
**~5.5 hours**

**Topics**
- 802.11 Standards
- WPA2/WPA3
- WLC & Lightweight APs (CAPWAP)
- Port Security
- DHCP Snooping

**Resources**
- 📘 Cisco Cert Guide Ch. 29–30 — Wireless & Security Fundamentals
- 🎥 Jeremy's IT Lab: Day 45–48 — Wireless Fundamentals, WLC
- 🖥️ Packet Tracer: Configure a WLC with a lightweight AP, associate a wireless client
- 📅 31 Days: Day 9 — Wireless · Day 8 — Security Features

**Lab**
Configure port security on a switch (max 2 MACs, violation shutdown). Verify with `show port-security interface`.

**Exam Tip**
CCNA wireless is concept-heavy. Focus on WLC modes, CAPWAP tunnels, and the differences between WPA2 and WPA3.

---

## Phase 6 — IPv6 & Automation (Weeks 12–13)

---

### Week 12 · IPv6 Addressing & Routing
**~5.5 hours**

**Topics**
- IPv6 Address Types (GUA, Link-Local, Multicast)
- EUI-64
- Stateless Autoconfig (SLAAC)
- OSPFv3 Overview

**Resources**
- 📘 Cisco Cert Guide Ch. 32–34 — IPv6
- 🎥 Jeremy's IT Lab: Day 49–52 — IPv6 Addressing & Routing
- 🖥️ Packet Tracer: Configure IPv6 static routes and SLAAC, verify with `show ipv6 interface brief`
- 📅 31 Days: Day 6 — IPv6

**Lab**
Assign IPv6 GUA and link-local addresses. Enable SLAAC. Verify a PC obtains an IPv6 address automatically.

**Exam Tip**
IPv6 link-local always starts with `FE80`. Know the 3 address types: Global Unicast, Link-Local, and Multicast. There are no broadcasts in IPv6.

---

### Week 13 · Automation, SDN & Network Programmability
**~5 hours**

**Topics**
- SDN & Controller-Based Networking
- REST APIs & JSON
- Ansible / Puppet / Chef (concepts)
- Cisco DNA Center

**Resources**
- 📘 Cisco Cert Guide Ch. 35–36 — Automation & Programmability
- 🎥 Jeremy's IT Lab: Day 55–58 — Automation, REST APIs, JSON, Python
- 🖥️ Packet Tracer: Explore automation/API labs if available in your version
- 📅 31 Days: Day 3 — Network Programmability

**Lab**
Review JSON data structures. Understand the difference between Northbound and Southbound APIs in SDN architecture.

**Exam Tip**
This domain is conceptual. Focus on: what REST APIs are, JSON syntax, the role of controllers, and high-level tool differences. Key fact: Ansible is agentless.

---

## Phase 7 — Review (Weeks 14–15)

---

### Week 14 · Full Review — Routing & Switching Deep Dive
**~5.5 hours**

**Topics**
- OSPF Troubleshooting
- STP & RSTP Review
- ACL Edge Cases
- Routing Table Analysis

**Resources**
- 📘 Cisco Cert Guide: Re-read chapters with the lowest practice test scores
- 🎥 Jeremy's IT Lab: Revisit Anki flashcards; re-watch weak areas
- 🖥️ Packet Tracer: Complete a full enterprise topology — switching + routing + security
- 📅 31 Days: Day 31–20 full re-read sweep

**Lab**
Build the largest topology you've done yet from scratch with no notes. Time yourself to configure OSPF, VLANs, and trunking.

**Exam Tip**
Track your wrong answers in practice tests. Categorize them by domain. Spend your time on your worst domain, not your best.

---

### Week 15 · Full Review — Security, WAN & IPv6
**~5.5 hours**

**Topics**
- NAT/PAT Scenarios
- IPv6 Routing Review
- Wireless Security
- Management Protocols

**Resources**
- 📘 Cisco Cert Guide: End-of-chapter review questions for Ch. 21–36
- 🎥 Jeremy's IT Lab: Complete any remaining lab exercises; flashcard review
- 🖥️ Packet Tracer: Complete the Cisco Skills Integration Challenges
- 📅 31 Days: Day 19–10 full re-read sweep

**Lab**
Configure NAT overload (PAT), then layer an ACL on top to restrict which inside hosts can be translated.

**Exam Tip**
Use Jeremy's Anki deck daily this week — even 10 minutes of flashcards reinforces retention significantly.

---

## Phase 8 — Final Prep (Week 16)

---

### Week 16 · Exam Simulation & Final Polish
**~5.5 hours**

**Topics**
- Full Practice Exams (timed)
- Weak Area Drills
- Subnetting Speed Drills
- Sim/Simlet Practice

**Resources**
- 📘 Cisco Cert Guide: Pearson Test Prep — take full timed practice exams
- 🎥 Jeremy's IT Lab: Exam tips videos; final review playlist
- 🖥️ Packet Tracer: Timed configuration drills — given a scenario, configure from scratch in 10 minutes
- 📅 31 Days: Day 9–1 — Final daily review leading up to exam day

**Lab**
Simulate exam conditions: 120-minute timed test, no notes. Review every wrong answer immediately after.

**Exam Tip**
Day before the exam: light review only, no new material. Sleep 8 hours. Budget ~70 seconds per question on exam day.

---

## Key Commands Reference

### Switching
```
show vlan brief
show interfaces trunk
show mac address-table
show spanning-tree
show etherchannel summary
show port-security interface <int>
```

### Routing
```
show ip route
show ip interface brief
show ip ospf neighbor
show ip ospf database
show ip protocols
```

### NAT & DHCP
```
show ip nat translations
show ip dhcp binding
show ip dhcp pool
```

### Security & Management
```
show running-config
show users
show line
show ip ssh
show logging
show ntp status
```

### IPv6
```
show ipv6 interface brief
show ipv6 route
show ipv6 ospf neighbor
```

---

## Subnetting Cheat Sheet

| CIDR | Subnet Mask | Hosts | Block Size |
|------|-------------|-------|------------|
| /24 | 255.255.255.0 | 254 | 1 |
| /25 | 255.255.255.128 | 126 | 128 |
| /26 | 255.255.255.192 | 62 | 64 |
| /27 | 255.255.255.224 | 30 | 32 |
| /28 | 255.255.255.240 | 14 | 16 |
| /29 | 255.255.255.248 | 6 | 8 |
| /30 | 255.255.255.252 | 2 | 4 |

**Formula:** Hosts per subnet = 2ⁿ − 2 (where n = host bits)

---

## OSI Model Quick Reference

| Layer | Name | PDU | Key Protocols |
|-------|------|-----|---------------|
| 7 | Application | Data | HTTP, FTP, DNS, DHCP |
| 6 | Presentation | Data | SSL/TLS, JPEG |
| 5 | Session | Data | NetBIOS, RPC |
| 4 | Transport | Segment | TCP, UDP |
| 3 | Network | Packet | IP, OSPF, ICMP |
| 2 | Data Link | Frame | Ethernet, 802.1Q |
| 1 | Physical | Bits | Cables, hubs |

---

## Study Tips

- **Subnetting** is the single most important skill — practice daily, not just in Week 4
- **Jeremy's Anki deck** is free and pairs perfectly with this plan — use it from Week 1
- **31 Days** works best as a daily 20-minute read in the final month (Weeks 13–16)
- **Packet Tracer** labs reinforce commands more than re-reading ever will — always lab after reading
- **Track wrong answers** by domain in your practice exams; double down on weak areas in Weeks 14–15
- The exam includes **Simlet questions** (troubleshoot a broken topology) — practice these specifically

---

*Good luck — you've got this. 🎓*