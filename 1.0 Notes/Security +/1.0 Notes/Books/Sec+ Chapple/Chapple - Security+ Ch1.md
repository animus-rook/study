---
type: book
title: CompTIA Security+ Study Guide with over 500 Practice Test Questions, 9th Edition
author: Mike Chapple, David Seidl
publisher: Sybex
isbn: "9781394211418"
source: https://learning.oreilly.com/library/view/comptia-security-study/9781394211418
phase: "{{phase}}"
status: Started
start_date: 06/15/2026
end_date: 06/15/2026
tags:
  - book
---
---

## 📝 Chapter Notes

### Chapter 1 — Today's Security Professional

#### Cybersecurity Objectives
- [[CIA Triad]]
	- Confidentiality
		- ensures unauthorized individuals are not able to gain access to sensative org data 
		- controls include firewalls, ACL's, ecryption
	- Integrity
		- ensures that no unauthorized modifications are made to data, intentionally or by accident
		- Controls include hashing
	- Availability
		- ensures that information and systems and resources are ready when users need them 
		- controls include fault tolerance, backups, 
- nonrepudiation - verifying that the perosn making the change canot deny it later
#### Data Breach Risks
- security incidents occur when on of the componets of the [[CIA Triad]] is breeched 
- incidents may occur intentionally (hacker), accidental (lost device), or an act of nature
##### The DAD Triad
- shows the three key threats to cybersecurity:
	- Disclosure
		- (data loss) exposure of sensitive org information
	- Alteration
		- unauthorized data modification
	- Denial
		- prevent legitimate access to resource or service
##### Breach Impact
Impact of security incident can be classified into certain risk categories
- **Financial Risk** - risk of monetary damage due to breach can be:
	- Direct -  Rebuilding data center or paying for recovery services
	- Indirect - plans being stolen by competitor leading to loss of revenue
- **Reputational Risk** - loss of goodwill, negative publicity
- **Strategic Risk** - company will be less effective at meeting its goals (long term/planned)
- **Operational Risk** - disruptions to organizations day to day functions (affects day to day)
- **Compliance Risk** - breach causes issues with regulatory compliance like HIPPA 
#### Implementing Security Controls
- Control objectives 
	- level of protection required to cover [[CIA Triad]]
	- desired security state (best case)
	- implementation left to [[security controls]]
##### Gap Analysis
- review of control objectives and [[security controls]] and seeing where the controls are lacking, gaps are treated as risks that need to be mitigated
##### Security Control Categories
organized based on how they achieve the objective also known as [[Mechanism of Action]]
- Technical - enforce controls in the digital space (firewall rules, ACL's, encryption)
- Operational - processes that we put in place (monitoring, access logs)
- Managerial - procedural mechanisms (risk assessments, security planning exercises )
- Physical - impact physical world, fences, burglar alarms
##### Security Control Types
- Preventive Controls - Stop issue before it occurs (firewall)
- Deterrent Controls - prevent an attacker from violating policies (guard dogs, fences, security cameras )
- Detective Controls - identify events that have already occurred
- Corrective Controls - remediate issues that have already occurred
- Compensating Controls - mitigate risks associated with exceptions to security policy
- Directive Controls - policies/procedures
#### Data Protection
 data can exist in 3 states 
 - At rest - stored data residing in hard drives, cloud other storage media
 - In Transit - in motion over the network
 - In use - data stored in memory, actively in use
  ##### Data Encryption
  - mathematical algorithms to protect against prying eyes
	  - Symmetric - shared key 
	  - Asymmetric - public and private key encryption 
  ##### Data Loss Prevention
  - Agent and agent less systems
  - Watermarking and pattern matching are also used in DLP systems
  ##### Data Minimization
  - reduce risk by reducing amount of sensitive information stored
  - deidentification transform data where PII is unidentifiable
  - Data obfuscation
	  - data is turned into form that cannot be retrieved
		  - Hashing
			  - transforms to a hash that can not be reversed
		  - tokenizatin
			  - replaces PII with a unique identifier, refrences back to a look up tabkle 
		  - Masking
			  - removinf or chaning caractors  ie X or *
##### Access Restrictions
- limit people or systems to access information or resources
- Geogrpahic restrictions - limit access based on user system location
- permission restrictions - limit based on users role or autherization 
- 

---
**Key points:**
- CIA Triad
- nonrepuudiation
- DAD Triad
- Risk Classification

**Commands / syntax I want to remember:**
```
```

**Questions this raised:**
- 

**Links to concepts:** 

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
