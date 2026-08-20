---
type: book
title: "Chapple - Security+ Ch3"
author: "{{author}}"
publisher: "{{publisher}}"
isbn: "{{isbn}}"
source: "{{url}}"
phase: "{{phase}}"
status: "not-started"
# status options: not-started | in-progress | complete
start_date: 
end_date: 
tags: [book, "{{phase}}"]
---

#  Chapple - Security+ Ch3

---

## Malware
 [[Malware]] software intentionally designed to cause harm to systems or devices, can also be used to collect information. 
 ### [[Ransomware]]
- [[Malware]] that takes over a computer or system and demands a ransom, types include
	 - crypto malware - encrypts files and demands ransom payment
	 - extortion is also part of it reporting to law enforcement or exposing sensitive information
	 - driven by phishing campaigns
 - [[(IOSs) indicators of compromise]]
	 - Command and control traffic 
	 - contact to known malicious IP addresses
	 - use of tools in abnormal ways to retain control of the compromised system
	 - Encryption of files
	 - Data exfiltration behaviors, including large transfers
	 - notices to end user with demands for ransom
	 - lateral movement to gain further access
 - Defenses/Mitigations
	 - Effective backup systems that is seperate from main system
	 - some [[Ransomware]] has been defeated and pre-exsisting tools cn be used to decrypt files. 
### [[Trojans]]
- [[Trojans]] are [[Malware]] that are disguised as a legitimate software once installed preform some type of malicious code execution 
- RATS are remote access trojans which give remote access to attackers
- requires user interaction
- [[(IOSs) indicators of compromise]]
	- Signatures for the specefic malware applications or downloadable files
	- Command and control system hostnames and IP addresses
	- Folders or files created on target device
- Defenses/Mitigations
	- awareness practices
	- controlling software and application downloads
	- Antimalware and EDR tools used as a last line of defense

>Botnets, BOTS, command and control
>Bots individuals systems under control from a command center
>botnets a collection of these bots

### [[Worms]]
- spread on their own
- can self install 
- spread via email attachments, file shares
- [[(IOSs) indicators of compromise]]
	- Known malicious files
	- downloads of additional components
	- contact to remote command and control systems
	- malicious behavior using system commands.
- Defenses/Mitigations
	- network level controls
	- Firewalls 
	- Intrusion prevention devices
	- network segmentation
	- Patching services
### [[Spyware]]
- [[Malware]] that is designed to gather information on an individual, organization or system
- Some can be innocuous but their is some that specifically targes sensitive data
- [[(IOSs) indicators of compromise]]
	- Known file fingerprints
	- malicious process
	- browser injection attacks
	- remote access/control indicators
- Defense/Mitigation
	- user awareness
	- software control
	- malware tools that are configured to detect spyware
### [[Bloatware]]
- unwanted applications already installed by manufacture 
- While not inhearntly malicious:
	- may be poorly written 
	- provide additional attack surface
	- may be vulnerable to exploitation
- Since not malicious doesnt have [[(IOSs) indicators of compromise]]
- Defense/Mitigation
	- Removal
	- User awareness
### [[Viruses]]
- malicious programs that self copy/replicate once activated
- require infection mechanisms to spread unlike worms
- Normally have both a trigger (what activates the [[virus]]) and payload (what the [[Viruses]] does)
- Varieties include:
	- Memory resident - remain in memory as device is running
	- non-memory resident - execute, spread and shutdonw
	- Boot sector - reside on boot sector of storage drive
	- Macro - use micros or code inside word processors 
	- email - as attachments or as part of email itself
- Fileless viruses
	- nothing is installed all is ran from memory
	- there may be registry edits to re-infect the system on reboots
	- no local file storage needed
- Defense/Mitigation
	- User awaness
	- antimalware detection tools
	- EDR (End Point Detection and Response)
### [[Keyloggers]]
- capture keystrokes from a keyboard, mouse movements, touchscreen inputs
- [[(IOSs) indicators of compromise]]
	- Files hashes and signatures
	- Exfiltration activity to command and control systems
	- process names
	- known reference URLs
### [[Logic Bombs]]
- not independent malware programs
- code/functions that will activate when certain conditions are met
- ==Requires code review to find==
### [[Rootkits]]
- Malware specifically designed to allow access through a backdoor
- Detection cna be calenging 
	- system can be trusted
	- needs to be checked from a known good device
	- rootkit removal is challenging need to rebuild system from back up
- [[(IOSs) indicators of compromise]]
	- file hashes and signatures
	- C/C domains and ip addresses
	- opening of ports or creation of reverse proxy tunnels
- Defense/mitigation
	- prevention is key as removal can be difficult 
	- 

**Core idea:**

**Key points:**
- 
- 
- 

**Commands / syntax I want to remember:**
```
```

**Questions this raised:**
- 

**Links to concepts/key terms:** 
[[Malware]]

---

## ⭐ Top Takeaways
*After finishing — what were the 3–5 most important things you learned?*

1. 
2. 
3. 

---

## 🔗 Concepts Created from This Book
*Link to any [[05-Concepts/]] notes you created while reading*

- 

---

## ❓ Unanswered Questions
*Things to look up, lab, or ask about later*

- 

---

## 🔁 How This Connects
*What labs, tools, or other notes does this feed into?*

- **Labs:** 
- **Tools:** 
- **Concepts:** 
- **Next book:** 
