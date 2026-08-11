#### Exam Topics Covered
[[Exam Objectives#1.0 Network Fundamentals (20%)| 1.0 Network Fundamentals]]
	[[Exam Objectives#^22df17|1.1 Explain the role and function of network components]]
		[[Exam Objectives#^7eb519|1.1.b Layer 2 and Layer 3 Switches]]
	[[Exam Objectives#^49b9f1|1.2 Describe characteristics of network topology architectures]]
		[[Exam Objectives#^4bc4d6|1.2.e Small Office/Home Office]]
[[Exam Objectives#^e0a2f1| 1.3 Compare interface and cabling types]]
		[[Exam Objectives#^55c678| 1.3.a Single-mode fiber, multimode fiber and copper]]
		[[Exam Objectives#^41e0b8| 1.3.b Connections (Ethernet shared media and point-to-point]]

---
## Key terms
[[10BASE-T]]
[[100BASE-T]]
[[1000BASE-T]]
[[Auto-MIDX]]
[[Broadcast address]]
[[Cladding]]
[[Core]]
[[Crossover Cable]]
[[Electromagnetic Interference]]
[[Ethernet]]
[[Ethernet Address]]
[[Ethernet Frame]]
[[Ethernet Link]]
[[Ethernet Port]]
[[Fast Ethernet]]
[[Fiber-Optic Cable]]
[[Frame Check Sequence]]
[[Gigabit Ethernet]]
[[IEEE]]
[[(MAC) Media Access Control addresses]]
[[Multimode Fiber]]
[[Network Interface Card (NIC)]]
[[RJ-45]]
[[Single-Mode Fiber]]
[[Straight-through Cable]]
[[Transceiver]]
[[Unicast Address]]
[[Wired LAN]]
[[Wireless LAN]]

---
# Notes
## An Overview of LAN's
- Term Ethernet refers to family of LAN Standards that together define physical and data-link layers
- IEEE - Institute of Electrical and Electronics Engineers define the standard
### Typical SOHO LAN's
- SOHO - Small office/home office
- Uses ethernet switch with ethernet cables
### Typical Enterprise LAN's
- Same  concept as a SOHO but on a bigger scale
### The Variety of Ethernet Physical Layer Standards
- Ethernet supports large variety of options for physical ethernet links
	- Can be optical or Copper based (UTP)

| Speed     | Common Name      | Informal IEEE Standard Name | Formal IEEE Standard Name | Cable type/Max Length |
| --------- | ---------------- | --------------------------- | ------------------------- | --------------------- |
| 10 Mbps   | Ethernet         | 10BASE-T                    | 802.3                     | Copper, 100m          |
| 100 Mbps  | Fast Ethernet    | 100BASE-T                   | 802.3u                    | Copper, 100m          |
| 1000 MBPS | Gigabit Ehternet | 1000BASE-LX                 | 802.3z                    | Fiber, 5000m          |
| 1000 Mbps | Gigabit Ethernet | 1000BASE-T                  | 802.3ab                   | Copper, 100m          |
| 10 Gbps   | 10 Gig Ethernet  | 10GBASE-T                   | 802.3an                   | Copper, 100m          |
### Consistent Behavior over All Links Using the Ethernet Data-Link Layer
- Ethernet LAN - Combination of user devices, LAN Switches and various cables connecting them. Key is that they all work together to deliver ethernet frames
	- [[Ethernet Frame]]
## Building Physical Ethernet LANs with UTP
- 3 most common ethernet standards
	- [[10BASE-T]]
	- [[100BASE-T]]
	- [[1000BASE-T]]
### Transmitting Data Using Twisted Pairs
- Each wire in the wire pair are used to create an electrical circuit. 
- To send data the to devices follow and encoding scheme 
- With encoding scheme the transmitter changes the the electrical signal over time, receiver if using same rules can interpret those changes as 1 or 0
	- ex. [[10BASE-T]] uses and encoding scheme that encodes a binary 0 as a transition from higher to lower voltage during the middle of 1/10,000,000th of a second interval 
- [[Electromagnetic Interference]]
### Breaking Down a UTP Ethernet Link
- [[Ethernet Link]]
- Most UTP use a Registered Jack-45 [[RJ-45]]
- [[Gigiabit Ethernet Interface Convertor (GBIC)]]
- [[Small Form Factor Pluggable (SFP)]]
- [[Small Form-Factor Pluggable Plus (SFP+)]]
### UTP Cabling Pinouts for 10BASE-T and 100BASE-T
#### Straight-Through Cable Pinout
- As a rule NIC transmit on pins 1 and 2 and receive on pins 3 and 6; switches receive on 1 and 2 and transmit on 3 and 6
- [[Straight-through Cable]] wiring
	NIC ----- Switch
	1 ----- 1
	2 ----- 2
	3 ----- 3
	6 ----- 6
#### Crossover Ethernet Cable Pinouts
- used if connecting device that use the same pins to transmit and receive
- diagram
- [[Crossover Cable]] wiring
1 ----- 3
2 ----- 6
3 ----- 1
6 -----2
#### Choosing the Right Cable Pinouts
- When to use each cable 
	- [[Crossover Cable]] - endpoints transmit on same pin pair
	- [[Straight-through Cable]] - endpoints transmit on different pin pairs
- [[10BASE-T]] and [[100BASE-T]] Pin Pairs used

| Transmits on Pins 1,2                      | Transmits on Pins 3,6 |
| ------------------------------------------ | --------------------- |
| PC NICs                                    | Hubs                  |
| Routers                                    | Switches              |
| Wireless Access Point (Ethernet interface) | -                     |
#### Automatic Rewiring with AUTO-MDIX
- introduced in 1998
- [[Auto-MIDX]] uses electrical impulses to detect incorrect pinouts and redirect impulses to correct pins
### UTP Cabling Pinouts for 1000BASE-T
- [[1000BASE-T]] using 4 pairs of wires 
- more advanced electronics to allow both ends to transmit and receive simultaneously
- Straight-Through
	- 1 ----- 1
	- 2 ----- 1
	- 3 ----- 3
	- 4 ----- 4
	- 5 ----- 5
	- 6 ----- 6
	- 7 ----- 7
	- 8 ----- 8
- Wire Pairs
	- A (1,2)
	- B (3,6)
	- C (4,5)
	- D (7,8)
- Crossover
	- 1 ----- 3
	- 2 ----- 6
	- 3 ----- 1
	- 4 ----- 7
	- 5 ----- 8
	- 6 ----- 2
	- 7 ----- 4
	- 8 ----- 5
## Building Physical Ethernet LANs with Fiber
- UTP cabling with is 100m restriction works for most cases however there are times where fiber may be used. (Greater distance less EMI)
### Fiber Cabling Transmission Concepts 
- Uses glass as the medium that transmits the data
- [[Fiber-Optic Cable]]
- Parts of a Fiber Optic Cable
	- [[Core]]
	- [[Cladding]]
	- Buffer
	- Strengthener
	- Outer Jacket
- ![[MUmode vs singlemode.png]]
- [[Multimode Fiber]]
- [[Single-Mode Fiber]]
### Using Fiber with Ethernet
- Using fiber with ethernet switches; switch needs to have a built in port that accepts fiber or a module port that allows changing of standard on port

|  Standard   | Cable Type | Max Distance* |
|:-----------:|:----------:|:-------------:|
|  10GBASE-S  |     MM     |     400m      |
| 10GBASE-LX4 |     MM     |     300m      |
| 10GBASE-LR  |     SM     |     10km      |
|  10GBASE-E  |     SM     |     30km      |
- ##### Comparisons between UTP, MM and SM Ethernet Cabling

| Criteria                                                    | UTP  | Multimode | Single-mode |
| ----------------------------------------------------------- | ---- | --------- | ----------- |
| Relative cost of cabling                                    | Low  | Medium    | Medium      |
| Relative cost of switchport                                 | Low  | Medium    | High        |
| Approximate Max Distance                                    | 100m | 500m      | 40km        |
| Relative Suceptability to interference                      | Some | None      | None        |
| Relative risk of copying from cable emissions (EFI Leakage) | Some | None      | None        |
## Sending Data in Ethernet Networks
- physical layer standards can differ however other parts of the ethernet standard work the same across differing physical mediums
### Ethernet Data-Link Protocols
- The ethernet data-link protocol defines the [[Ethernet Frame]]
- ![[802.3 ethernet frame.png]]
- Header encompasses preamble to type
- Trailer is the FCS or Frame check sequence
- ##### Ethernet Header and Trailer 

| Field                                                              | Bytes   | Description                                                                                                                    |
| ------------------------------------------------------------------ | ------- | ------------------------------------------------------------------------------------------------------------------------------ |
| Preamble                                                           | 7       | Synchronization                                                                                                                |
| Start Frame Delimiter (SFD)                                        | 1       | Signifies that the next byte will be start of destination [[(MAC) Media Access Control addresses]]                             |
| Destination [[(MAC) Media Access Control addresses\| MAC Address]] | 6       | Who is the intended recipient of this [[Frame]]                                                                                |
| Source [[(MAC) Media Access Control addresses\|MAC Address]]       | 6       | who the sender is                                                                                                              |
| Type                                                               | 2       | Defines the type of protocol inside the frame usually IPv4 maybe IPv6                                                          |
| Data and Pad                                                       | 46-1500 | Holds data from a higher layer; normally a IPv4 or IPv6 [[Packet]] Sender will add padding to meet minimum 46 byte requirement |
| Frame Check Sequence (FCS)                                         | 4       | used by receiving [[Network Interface Card (NIC)]] to identify transmission errors                                             |
> [!tip]
> 802.3 limits the data portion of a 802.3 frame to the 45-1500. Term [[Maximum Transmission Unit (MTU)]] defines the layer 3 max packet size over a medium. Since layer 3 resides in data portion 1500 bytes us largest IP [[Maximum Transmission Unit (MTU)]] allowed over ethernet

#### Ethernet Addressing
- Ethernet Address AKA [[(MAC) Media Access Control addresses]]
	- 6 byte long
	- 48 bit
	- normally shown in 12 digit hexadecimal
- Most of the time the [[(MAC) Media Access Control addresses]] represents a single port or NIC refered to as [[Unicast Address]]
- Mac addresses are unique the IEEE assigns all vendors a 3 byte organizational unique identifier (OUI) then the vendor must assign a unique value for the last 3 bytes that has not been used with the OUI. 
> [!tip]
> IEEE calls universal [[(MAC) Media Access Control addresses|MAC Addresses ]] global MAC addresses

##### Unicast Ethernet address

|            | Organizational Unique Identifier (OUI) | Vendor Assigned (NIC Cards, Interfaces) |
| ---------- | -------------------------------------- | --------------------------------------- |
| Example    | 00:40:3f                               | 4C:04:AB                                |
| hex Digits | 6                                      | 6                                       |
| bits       | 24 bits                                | 24 bits                                 |
- [[Broadcast address]]
- [[Multicast Addresses]]
#### Identifying Network Layer Protocols with the ethernet type field
- basically identifies the type of network layer (layer 3) packet inside the ethernet frame
- Most common network protocols are both from TCP/IP and not vendor specific IPv4 and IPv6
- IEEE manages list of Ethertype values
#### Error detection with FCS
- Ethernet also has a way to check if frames bits have been changed while crossing over a link
- [[Frame Check Sequence]]
- Sender applies a complex math formula to frame then stores it in the FCS field. When the sender receives it it applies same math formula and checks answer vs what is in the FCS field. 
- This is **error detection** and not *error correction*
### Sending Ethernet Frames with Switches and Hubs
- More modern LANs with ethernet switches can operate in full duplex logic faster and simpler than half duplex logic
#### Sending in Modern Ethernet LANs using full duplex
- Half Duplex - Device needs to wait before sending a frame if currently receiving
- Full Duplex - Device can send and receive at same time
- Switches Full duplex
#### Using Half duplexes with LAN Hubs
- Hubs
	- Considered Layer one devices
	- Data is forwarded not on *data-link* but **physical layer**
	- Collisions can happen uses hubs
- Half Duplex assists with collisions using **CSMA/CD** (carrier sense multiple access with collision detection)
	- How it works
		- 1. Device with a frame to send listens until ethernet is not being used
		- 2. If not busy sender begins sending their frame
		- 3. Sender listens to see if there sending causes collisions if yes;
			- Send a jamming signal to all nodes that a collision happened
			- independently choose a random time to wait, then try again
			- starts again