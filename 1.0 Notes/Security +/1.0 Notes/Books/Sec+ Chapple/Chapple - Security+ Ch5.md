---
type: book
title: Untitled
author: "{{author}}"
publisher: "{{publisher}}"
isbn: "{{isbn}}"
source: "{{url}}"
phase: "{{phase}}"
status: not-started
start_date:
end_date:
tags:
  - book
---

# 📖 Chapple - Security+ Ch5


---

## 📝 Ch 5 Security Assessment and Testing

### Vulnerability Management
- Vulnerability management is crucial in identifying, prioritizing and remediating vulnerabilities in the environment using:
	- Vulnerability scanning to find new vulnerabilities as they happen
#### Identifying Scan Targets
- organizations may choose to cover all systems in their scanning process, whereas others may scan systems differently (or not at all) depending on the answers to many different question
#### Determining Scan Frequency
- Administrators may designate a schedule that meets their security, compliance, and business requirements.
- Factors influencing to determine frequency:
	- Orgs [[risk appetite]], how much risk the org is willing to accept
	- [[regulatory requirements]] may dictate how often scans should be preformed to maintain compliance
	- [[technical constraints]] what system resources may allow/limit
	- [[business constraints]] making sure scans do not disrupt the day to day operations
	- [[licensing limitations]] - what does scanning software allow 
#### Configuring Vulnerability Scans
##### Scan Sensitivity Levels
- the types of checks that the scanner will perform
##### Supplementing Network Scans
- Network scanners may be blocked by firewalls, so supplementing with other scanners
##### Scan Perspective
- scan from different point in network 
	- Either side of DMZ
	- Internal/External
##### Scanner Maintenance
- making sure the vulnerability feeds are up to date
	- making sure scanning software is also up to date to prevent breeches
##### Scanner Software
- patch scaning software to remove that as a liability
##### Vulnerability Plug in feeds
- ensure that vulnerability feeds are updated regularly on software 
	- [[SCRAP (Security Automation Protocol)]] led by NIST standerdize approach from communicating security information, standards include:
		- **Common Configuration enumeration (CCE)** - provides standard naming for system configuration issues
		- **Common Platform Enumeration (CPE)** - standard naming for product names and versions 
		- **Common Vulnerability Scoring system (CVSS)** - standards for describing the severity 
		- **Extensible configuration checklist description format (XCCDF)** - language for checklist and checklist results
		- **Open vulnerability and assessment kanguage (OVAL)** - language for specefying low level testing procedures 
#### Vulnerability scanning tools
- Network vulnerability scanners
- application scanners
- web application scanners
##### Infrastructure Vulnerability scanner 
- network vuln scanner reaches out to systems connected to network 
- Examples include
	- Tenables Nessus
	- Qualys Vulnerability scanner 
	- Nexpose
	- Open vas
##### Application Testing
- commonly uses in software development
- uses three techniques to discover issues
	- Static testing - analyzes without code execution
	- Dynamic - executes code and runs through all the interfaces
	- Interactive testing - combo of both 
##### Web Application Scanning
- pecialized tools used to examine the security of web applications. These tools test for web-specific vulnerabilities, such as SQL injection, cross-site scripting (XSS), and cross-site request forgery (CSRF) vulnerabilities
#### Reviewing and interpreting Scan reports
##### Understanding CVSS
- [[Common vulnerability scoring system (CVSS]] has various measures to score a vulnerability
- normally looks like this `CVSS:3.0/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:N/A:N`
- 8 measures are 
	- **Attack Vector Metric (AV)**
		- How can attacker explot![[Pasted image 20260625101833.png]]
	- **Attack Complexity Matrix (AC)
		- exploit difficulty ![[Pasted image 20260625102021.png]]
	- **privleges required matrix(pr)**
		- account typoe needed to explot admin/standard ![[Pasted image 20260625102232.png]]
	- **User Interaction metric (UI)**
		- Does another human need to do something to exploit![[Pasted image 20260625102335.png]]
	- **Confidentiality Metric (c)**
	- ![[Pasted image 20260625102557.png]]
	- **Integrity metric(i)**
	- ![[Pasted image 20260625102641.png]]
	- **Availability etric (a)**
	- ![[Pasted image 20260625102658.png]]
	- **Scope metric**
	- ![[Pasted image 20260625102715.png]]
##### Severity rating scale
![[Pasted image 20260625110832.png]]
### Vulnerability Classification
- genrela categories vuln scan may find
	- Patch management - runnn latest OS
	- Legacy platforms - unsupported OS
	- Weak configurations
		- default settings
		- default creds
		- open service ports
		- open permissions
	- Error messages - debug mode giving out to muck info when scanned 
	- insecure protocols- ex include telenet, FTP
	- Weak encryption
		- weak algorithim or key
### Penetration Testing
- 4 types 
	- physicla attack physical controls of an org
	- Offesnive - simulate real world attacks 
	- Deffesnive - assessing effectiveness of security policies
	- Intergrated - a mix of both
- how much information is given to tester
	- known environment
		- pretty much given keys to kingdom, while very thorough does not give clear picture as what an outsider would see
	- unknown environment
		- replicate what an attacker would encounter
	- partially known 
		- mix of the two may ie may give diagrams but not creds
- Rules of engagement
	- timeline - when can testing occur over how long and time of day etc
	- scope - what is included and excluded from test
	- data handeling requirments - should data be encrypted or not and disposing of findings 
	- behaviors - what is target going to do
	- resources
	- legal concearns
	- communication 
#### penetration test phases
- reconnaissance
	- passive vs active
		- passive does not engage targe
		- active does
- running the test
	- initial access
	- prilege escalation
	- pivoting/lateral movement
	- persistence
- Cleaning up
	- present results and remove traces and persistence from the network
### Audits and Assessments
- 3 major components of assessment program
	- Security Test
		- verify control is functioning properly 
			- bug bounties are a form of a responsible disclosure program
	- security assessments
		- comprehensive reviews of the security of a system, application, or other tested environment.
	- security audits
		- similar to a security assessment but must be conducted by an external entity

### Vulnerability life cycle 

---

## 🔗 Concepts Created from This Book
*Link to any [[05-Concepts/]] notes you created while reading*

- 

---
