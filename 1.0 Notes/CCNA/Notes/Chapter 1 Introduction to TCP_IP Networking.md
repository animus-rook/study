#### Exam Topics Covered

[[Exam Objectives#1.0 Network Fundamentals (20%)| 1.0 Network Fundamentals]]
[[Exam Objectives#^e0a2f1| 1.3 Compare interface and cabling types]]
[[Exam Objectives#^55c678| 1.3.a Single-mode fiber, multimode fiber and copper]]
[[Exam Objectives#^41e0b8| 1.3.b Connections (Ethernet shared media and point-to-point]]

---
### Key terms

[[Segment]]
[[Same-layer interaction]]
[[adjacent-layer interaction]]
[[Frame]]
[[De-encapsulation]]
[[Encapsulation]]
[[Networking Model]]
[[Packet]]
[[Segment]]

---

## Notes

In networking diagrams the cloud normally represents details not important to the diagram 
## History Leading up to TCP/IP
- Network models began as vendor specific
- International Organization for Standardization came out with the OSI Model
- DOD contracted research developed TCP/IP
- In the 1990's both OSI model and TCP/IP model where in use
- By end of the 1990's OSI fell to wayside with TCP/IP dominating
### Overview of TCP/IP Model
- TCP/IP References and defines a large collection of protocols that allow devices to communicate
- Protocols are defined as RFC (Request for Comments)
- TCP/IP avoids repeated work by simply referring to standards/protocols provided by 3rd party
	- Ex. ethernet is defined by as RFC but refers to IEEE ethernet as an option

| TCP/IP model Layers                                                      |
| ------------------------------------------------------------------------ |
| Application                                                              |
| Transport                                                                |
| Network AKA IP Layer - Responsible for delivering data across whole path |
| Datalink - focuses on rules that control use of physical link            |
| Physical - Focuses how to transmit data over link                        |
- Different computer components implement different protocols/standards
- Example layers and Protocols
	- Application - HTTPS,POP3,SMTP
	- Transport - TCP/UDP
	- Network - IP,ICMP
	- Datalink - Ethernet, 802.11
### TCP/IP Application Layer
- App layer does not define application, Defines services that the application needs
	- Provides interface between software running on computer and network itself
	- Web Browser is an example
#### HTTP Overview
- Hypertext Transfer Protocol
- Developed 1990s
- URL - Uniform Resource Locators
- URI - Uniform Resource Identifier
- Protocols generally use headers to put info used by that protocol
	- 200 - OK
	- 404 - Not Found
### TCP/IP Transport Layer
- 2 most common used protocols
	- TCP - Transmission Control protocol
		- Error recovery based
		- Each layer Provides service to layer above it
		- To recover from errors TCP uses concept of Acknowledgements
	- UDP - User Datagram Protocol
#### Same Layer & Adjacent Layer

| Adjacent Layer Interaction                                                                                                                                                                                  | Same Layer Interaction                                                                                                                                                   |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| On a single computer, one lower layer provides a service to the layer just above. The software or hardware that implements the higher layer requests that the next lower layer perform the needed function. | The two computers use a protocol to communicate with the same layer on another computer. The protocol defines a header that communicates what each computer wants to do. |
### TCP/IP Network Layer
- Network layer hold small number of protocols
- Only one  major protocol
	- IP (Internet Protocol)
		- Used for features such as addressing and routing
#### IP Addressing Basics

Dotted Decimal notion 0.0.0.0
Example Google DNS is 8.8.8.8
>[!note] More Info
>To make Internet addresses easier for human users to read and write, IP addresses are often expressed as four decimal numbers, each separated by a dot. This format is called "dotted-decimal notation." Dotted-decimal notation divides the 32-bit Internet address into four 8-bit (byte) fields and specifies the value of each field independently as a decimal number with the fields separated by dots

### TCP/IP Data Link and Physical Layer
- Defines protocols and hardware required to deliver data across some physical network
- Some protocols define both Datalink and Physical Layer functions
- Physical Layer defines cabling as well as how energy passes through it
- Sending IP Packets the host/router uses link layer details to send packet on

#### Ethernet Frame
- Made up of:
	- Ethernet Header
	- IP Packet
	- Ethernet Trailer
- Frame
	- IP Packet with Ethernet Header and Trailer
- De-encapsulate 
	- At this level it is the removal of the Ethernet Header/Trailer leaving IP Packet
### Data Encapsulation Terminology


> [!NOTE] Encapsulation
> Refers to the process of putting headers (somtimes trailers) around some data

Process that TCP/IP host sends data viewed as a 5 step process

1. Create and encapsulate the app data with any required application layer headers
2. Encapsulate the data supplied by app layer inside a transport layer header
3. encapsulate data supplied by transport layer inside a network layer (IP) header
4. encapsulate data provided by network layer inside a data link layer header/trailer
5. send bits
### Names of TCP/IP Messages
 

| Layer       | "Frame"                         |
| ----------- | ------------------------------- |
| Application | Data                            |
| Transport   | TCP+Data                        |
| Network     | IP+TCP+Data                     |
| Data Link   | Data Link+IP+TCP+Data+Data Link |
| Physical    | Transmit Bits                   |
>[!note] Network Model
>Sometimes Protocol Data Unit will be referred to any message defined by a protocol. TCP Segment, IP Packet and Ethernet frame are all PDU's
### OSI Network Model and Terminology
TCP/IP won out over OSI however a lot of OSI model is still used. 
### Comparing OSI and TCP/IP Layer Names and Numbers

| Layer | OSI          | Layer | TCP/IP<br>(Common) | Layer | TCP/IP<br>(RFC 1122) |
| ----- | ------------ | ----- | ------------------ | ----- | -------------------- |
| 7     | Application  |       |                    |       |                      |
| 6     | Presentation |       |                    |       |                      |
| 5     | Session      | 5-7   | Application        |       |                      |
| 4     | Transport    | 4     | Transport          | 5-7   | Application          |
| 3     | Network      | 3     | Network            | 4     | Transport            |
| 2     | Data Link    | 2     | Data Link          | 3     | Internet             |
| 1     | Physical     | 1     | Physical           | 1-2   | Link                 |
**RFC 1122** - Original four layer model prior to use of current 5 layer. 



> [!warning] Network Model
> Genric term refering to any set of protocols/standards collected together that when followed allows devices on a network to commuinicate.




