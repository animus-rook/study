#### Exam Topics Covered
[[Exam Objectives#1.0 Network Fundamentals (20%)| 1.0 Network Fundamentals]]
	[[Exam Objectives#^22df17|1.1 Explain the role and function of network components]]
		[[Exam Objectives#1.1 Explain the role and function of network components| 1.1a Routers]]
	[[Exam Objectives#1.2 Describe characteristics of network topology architectures| 1.2 Describe characteristics of Network Topology architectures]]
		[[Exam Objectives#1.2 Describe characteristics of network topology architectures| 1.2.d WAN]]
		
---
## Key terms

[[ARP - Address Resolution Protocol]]
[[Default router (default gateway)]]
[[DNS - Domain Name Service]]
[[Ethernet Line Service (E-Line)]]
[[Ethernet WAN]]
[[HDLC]]
[[Hostname]]
[[IP Address]]
[[IP Network]]
[[IP Packet]]
[[IP Subnet]]
[[Leased Line]]
[[Ping]]
[[Routing Protocol]]
[[Routing Table]]
[[Serial Interface]]
[[Subnetting]]
[[Telco]]
[[WAN - Wide Area Network]]


---

# Notes
# Wide Area Networks
- [[WAN - Wide Area Network]] Technologies define the layer 1 (physical) standards and Layer 2 (Date-link)  protocols used to communicate over long distances
## Leased-Line WANs
- lightning bolt representing [[WAN - Wide Area Network]] link normally means leased line
- 2 common data link protocols in leased lines [[HDLC]] and PPP
### Physical details of Leased Lines
- [[Leased Line]] is a physical layer service, delivering Bits in both directions, using a predetermined speed using full-duplex logic
- 2 pairs of wires, one pair for each direction allowing full-duplex
- A physical path must exist between both router locations
- [[Telco]] creates a large complex network that appears as a cable connecting both routers
- Telcos equipment is houses in a "Central Office"
- Leased lines have been around for a while so new terms have been given to it

| Name                                     | Meaning or Refrence                                                                                                                                                   |
| ---------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Leased circuit, Circuit                  | The words line and circuit are often used as synonyms in telco terminology; circuit makes reference to the electrical circuit between two endpoints                   |
| Serial link, Serial Line                 | The words link and line are also often used as synonyms. Serial in this case refers to the fact that the bits flow serially and that routers use [[Serial Interface]] |
| Point to point link, Point to point line | These terms refer to the fact that the topology stretches between two points, and two points only                                                                     |
| T1                                       | Specific leased line that transmits data at 1.544 Mbps                                                                                                                |
| WAN Link, Link                           | General no reference to any specific tech                                                                                                                             |
| Private Line                             | Refers to fact that data sent over the line cannot be copied by other telco customers                                                                                 |
### Data-Link Details of Leased Lines
- Routers on each end of the leased lines use [[HDLC]] (High-Level Data Link Control) or Point to Point Protocol (PPP)
- Leased Line provides a layer 1 service
- Leased line itself does not define a data-link layer protocol
- [[HDLC]] and PPP provide similar functions to Ethernet Data-link protocols
- PPP (1990s) is newer than [[HDLC]] (1970s)
- [[HDLC]] Frame Format

| Bytes    | Frame Components         |
| -------- | ------------------------ |
| 1        | Flag                     |
| 1        | Address                  |
| 1        | Control                  |
| 2        | Type                     |
| Variable | Data                     |
| 2        | [[Frame Check Sequence]] |
- [[HDLC]], PPP and [[Ethernet]] fields

| [[HDLC]]/PPP             | Ethernet                 | Desc.                                                                                                                    |
| ------------------------ | ------------------------ | ------------------------------------------------------------------------------------------------------------------------ |
| Flag                     | Preamble, SFD            | List a recognizable pattern of bits so receiving nodes are aware a new frame is on its way                               |
| Address                  | Destination Address      | The Address of destination device, assumed in leased line point-to-point topologies and they are “no other destinations” |
| Control                  | N/A                      | No longer in use                                                                                                         |
| Type                     | Type                     | What type of layer 3 packet is in data section of the fame                                                               |
| [[Frame Check Sequence]] | [[Frame Check Sequence]] | Field used for error detection                                                                                           |
### How Routers Use a WAN Data Link
- TCP/IP Network layer is focused on the forwarding of [[IP Packet]]
- PC1’s network layer (IP) logic tells it to send the packet to a nearby router (R1).
- Router R1’s network layer logic tells it to forward (route) the packet out the leased line to Router R2 next.
- Router R2’s network layer logic tells it to forward (route) the packet out the LAN link to PC2 next.
- ![[Encapsulation and Decapsulation Routers.png]]
- Negatives of leased lines
	- higher cost
	- longer lead times for installation
	- lower speeds as compared to newer ethernet WANs
## Ethernet as a WAN Technology
- Many WAN Service providers (SP) provide ethernet WANS
- The fiber ethernet link leaves a customers location and arrives at a location knows as the (PoP) point of presence. 
### Ethernet WANs that Create a Layer 2 Service
- Logically behaves like a point-to-point connection between two routers
- Physically behaves as if a physical fiber link existed between the two routers
- This [[WAN - Wide Area Network]] service referred to as:
	- [[Ethernet WAN]]
	- Ethernet - Point to point link: in reference to the topology of an [[Ethernet WAN]] link with once connection and router on each side
	- [[Ethernet Line Service (E-Line)]] - Term from the (MEF) Metro Ethernet Forum
	- Ethernet over MPLS (EoMPLS) - refers to multiprotocol label switching, used to create the [[Ethernet]] service for the end user
### How Routers Route IP Packets using WAN Links
- Packet over a [[Ethernet WAN]] link
	- PC encapsulates [[IP Packet]] in an [[Ethernet Frame]] 
	- [[Ethernet WAN]] link uses [[Ethernet]] for both Layer 1 and 2 Functions
	- ![[Pasted image 20250106141236.png]]
	- To send the [[IP Packet]] to Router R1 , PC1 encapsulates (inserts) the IP packet in an Ethernet frame that has the ==destination [[(MAC) Media Access Control addresses]] of R1==.
	- Router R1 de-encapsulates (removes) the IP packet from the [[Ethernet Frame]] and encapsulates (inserts) the packet into a new [[Ethernet Frame]], with a new Ethernet header and trailer. The ==destination MAC address is R2’s G0/0 MAC address==, and the ==source MAC address is R1’s G0/1 MAC address==. R1 forwards this frame over the Ethernet WAN service to R2 next.
	- Router R2 de-encapsulates (removes) the [[IP Packet]] from the [[Ethernet Frame]], encapsulates (inserts) the packet into an [[Ethernet Frame]] that has destination [[(MAC) Media Access Control addresses]] of PC2. forwarding [[Ethernet Frame]] to Destination PC
- 
# IP Routing 
- At Network Layer of TCP/IP model 2 options to use that all other network layer functions will use
	- IP version 4 (IPv4)
	- IP Version 6 (IPv6)
	- Internet Protocol (IP) job is to route data, using [[IP Packet]]s
		- Not concerned with physical transmission of data. 
		- Specifies how packets travel over a TCP/IP  network
- [[Routing Protocol]]
## Network Layer Routing (forwarding) Logic
- Routers and end-users (hosts) work to perform IP routing
- Host OS has TCP/IP software, used to choose where IP packets go
### Host Forwarding logic: Send the packet to default router
- Host does some analysis and realizes that destination is not on same LAN and so forwards to [[Default router (default gateway)]]
- Sender sends a data link layer 2 addressing to ensure the router receives the packet
### R1 and R2's Logic: Routing Data across the Network
- Routers use similar process to route the packet IP [[Routing Table]]
	- [[Routing Table]] list:
		- IP Address grouping as [[IP Network]]s and [[IP Subnet]]s
- Router compares destination IP to entries in the table, matching entries also list directions on where to forward packet next. 
## How Network Layer Routing uses LANs and WANs
- Routers Internal Network layer routing 
	- Use data link[[Frame Check Sequence]] field to validate frame, if their are errors [[Frame]] is discarded
	- Discard old data link header and trailer, [[IP Packet]] remains
	- [[IP Packet]] destination [[IP Address]]  checked against routing table to find route, route identifies outgoing interface as well maybe IP address of next hop
	- Encapsulate the [[IP Packet]] inside a proper new data link header and trailer and forward [[Frame]]
	- {{figure 3-11}}
- Routers use [[ARP - Address Resolution Protocol]] to learn what data link layer to use
## How IP Addressing Helps IP Routing
- Any interface that expects to receive an [[IP Packet]] needs and [[IP Address]]
### Rules for Groups of IP Addresses (Networks and subnets)
- [[IP Address]] used on same physical network are part of same group IP calls these groups:
	- [[IP Network]]
	- [[IP Subnet]]
- Grouping IP's allows routing tables to be smaller as an entry can list an [[IP Network]] or [[IP Subnet]] vs each individual [[IP Address]]
- Two foundational rules of [[Subnetting]]
	- Two [[IP Address]] not separated from one another by a router must be in same subnet (group)
	- Two [[IP Address]] separated by at least one router must be in different subnets
### The IP Header
- Routing process makes use of IPv4 header lists:
	- 32 bit source IP 
	- 32 bit destination IP
## How IP Routing Protocols help IP Routing
- IP Supports a small amount of routing protocols, however most share some general features
	- Routers independently of [[Routing Protocol]], adds a route to its [[Routing Table]] for each subnet connected to it
	- Routers [[Routing Protocol]] will tell its neighbors about the routes it knows, including routes learned from other devices
	- [[Routing Protocol]] listens to messages from neighbor routers to learn routes
## Other Network Layer Features
Other protocols and standards described by RFC's play critical functions in network layer as well
### Using Names and the Domain Name System
- [[DNS - Domain Name Service]] is used to resolve [[Hostname]] into [[IP Address]]
### The Address Resolution Protocol
- [[ARP - Address Resolution Protocol]] is used to discover the [[(MAC) Media Access Control addresses]] to use in data link layer [[Frame]]s
- Sends an ARP request as an ethernet broad cast then waits for Arp reply
- Will store in the MAC table or cache, entries do time out to save space
### ICMP Echo and the Ping Command
- Ping - Primary tool to test basic network connectivity
- Uses ICMP (Internet Control Message Protocol) to send *ICMP Echo Requests* and *ICMP Echo replies*
- ICMP does not rely on applications to run, so really only test packets moving back and forth layers 1,2,3 of the OSI model.
