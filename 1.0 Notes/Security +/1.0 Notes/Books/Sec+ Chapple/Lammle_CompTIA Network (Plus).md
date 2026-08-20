---
type: book
title: CompTIA Network+
author: Todd Lammle, Jon Buhagiar
publisher: Sybex
isbn: "{{9781394235612}}"
source: https://learning.oreilly.com/library/view/comptia-network-study/9781394235605
phase: Phase 1
status: Started
start_date: 06/10/26
end_date:
tags:
  - book
---


---

## 📝 Chapter Notes

### Chapter 1 — Introduction to Networks

#### What is a Network
  - A network is a two or more connected computers than share resources with one another
  - Network Types
	  - MAN (Metropolitan area network) - a networking covering a metro area
	  - [[WAN - Wide Area Network]]
	  - LAN (local area network) - normally restricted to a particular physical location connected by a switch 

#### Physical Network Topologies

#### topology Selection, Backbones and Segments 
- traffic flow
	- North-South Data is flowing to and from our org to the internet
	- East-West - Traffic flow between org infrastructure 

**Questions this raised:**
- Can North-South be considered entry for external attackers and East-west as lateral movement?

**Links to concepts:**
[[North South Traffic Flow]]
[[East-West Traffic Flow]]

---
### Chapter 2 - The Open Systems Interconnection (OSI) Reference Model

#### Internetworking Models
- OSI Model has seven Layers
![[OSI Summary.png]]


![[OSI Detailed.png]]
- Applications layer - where users actually interact
	- Browsers don't live in app layer but requires access to app layers resources
	- Think SFTP and TFTP
- Presentation Layer
	- Presents data to app layer in a way app layer can understand
	- Data compression, encryption happen at this layer
- Session Layer
	- set up and tear down of sessions at presentation layer
- Transport layer
	- TCP/UDP operate here
	- Provides the end to end data transport
	- TCP three way handshake also happens here
- Network Layer
	- logical addressing
	- Data Packets
	- Route update packets
	- Routers
		- Routers, by default, won't forward any broadcast or multicast packets.
		- Routers use the logical address in a Network layer header to determine the next-hop router to forward the packet to.
		- Routers can use access lists, created by an administrator, to control security on the types of packets that are allowed to enter or exit an interface.
		- Routers can provide layer 2 bridging functions if needed and can simultaneously route through the same interface.
		- Layer 3 devices (routers, in this case) provide connections between virtual LANs (VLANs).
		- Routers can provide quality of service (QoS) for specific types of network traffic.
- Data Link Layer
	- [[(MAC) Media Access Control addresses]]
- Physical Link Layer
	- Send and receive bits
	- Transmission media 
#### Introduction to encapsulation
- ![[encapsulation.png]](Data encapsulation)

#### Modulation Techniques

**Questions this raised:**
- Modulation technicques as an attack surface?

**Links to concepts:**
[[(MAC) Media Access Control addresses]]

---

## ⭐ Top Takeaways
*After finishing — what were the 3–5 most important things you learned?*

1. 7 layers in OSI model
2. Key terms Datagrams, segments, packets frames
3. encapsulation

---

## 🔗 Concepts Created from This Book
*Link to any [[05-Concepts/]] notes you created while reading*

- [[East-West Traffic Flow]]
- [[North South Traffic Flow]]

---


---
