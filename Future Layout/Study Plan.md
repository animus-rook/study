# 🔎 Security+ → CySA+ → BTL1 → Detection Engineer — 7-Month Roadmap

> **Anthony Rios** | `riosinfra` | 5–10 hrs/week | Aug 2026 – Feb 2027
> Targeting: **Detection Engineer** (entry-level) + **SOC Analyst Tier 1/2** as a fallback wave

---

## 📋 Table of Contents

- [My Profile](#my-profile)
- [The Three Certifications, and Why This Order](#the-three-certifications-and-why-this-order)
- [Gap Analysis](#gap-analysis)
- [Milestone Overview](#milestone-overview)
- [Phase 1 — Security+ (SY0-701), Months 1–2](#phase-1--security-sy0-701-months-12)
- [Phase 2 — CySA+ (CS0-004), Months 3–5](#phase-2--cysa-cs0-004-months-35)
- [Phase 3 — Blue Team Level 1 (BTL1), Months 6–7](#phase-3--blue-team-level-1-btl1-months-67)
- [Phase 4 — Home SOC Capstone + Apply, Month 8](#phase-4--home-soc-capstone--apply-month-8)
- [Homelab SOC Projects](#homelab-soc-projects)
- [Resources & Links](#resources--links)
- [Note-Taking Templates](#note-taking-templates)
- [Application Strategy](#application-strategy)

---

## My Profile

|                      |                                                                       |
| -------------------- | --------------------------------------------------------------------- |
| **Current Role**     | Technology Service Technician — Hacienda La Puente USD                |
| **Experience**       | 5+ years production infrastructure, MDM (JAMF enterprise), networking |
| **Study Time**       | 5–10 hrs/week (flexible — scale sessions up on lighter work weeks)    |
| **Hardware**         | ZimaBoard 832 (8GB RAM) homelab                                       |
| **Primary Target**   | Detection Engineer                                                   |
| **Secondary Target** | SOC Analyst Tier 1/2                                                  |

### Certifications Completed

- [x] Google IT Support Professional Certificate (Coursera)
- [x] ISC2 Certified in Cybersecurity (CC) — direct overlap with Security+ Domain 1
- [x] Google Project Management Certificate (Coursera)
- [x] Calbright College Network Technology Certificate (Jan 2026)
- [x] Mac OS & iOS Certified (Apple)

### Certification Targets, In Order

- [ ] CompTIA Security+ (SY0-701) — Target: End of Month 2
- [ ] CompTIA CySA+ (CS0-004) — Target: End of Month 5
- [ ] Blue Team Level 1 (BTL1) — Target: End of Month 7

---

## The Three Certifications, and Why This Order

These aren't three unrelated study sprints stacked together — each one hands off directly to the next.

| Cert           | Level        | What it actually validates                                                   | Format                                              |
| -------------- | ------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------ |
| Security+  | Entry        | Vocabulary and concepts — threats, architecture, operations, governance         | 90 questions / 90 min, multiple-choice + PBQs, $404-425 |
| CySA+      | Intermediate | Applying that vocabulary — SOC operations, vulnerability management, IR, reporting | 85 questions / 165 min, multiple-choice + PBQs, $404-425 |
| BTL1       | Practical    | Actually doing the job — a real 24-hour incident investigation, no multiple choice | 20 task-based challenges, 24 hrs, open-book, ~$490      |

> CySA+ officially recommends ~4 years of SOC/vulnerability-analyst experience — most candidates without that background go straight from Security+ into CySA+ anyway, and the two exams overlap enough (log analysis, threat hunting, MITRE ATT&CK, vulnerability scoring) that Security+ concepts carry over directly instead of being wasted. BTL1 has no prerequisite at all, but it assumes you already know why an alert matters (Security+/CySA+) so you can spend the 24-hour exam on how to investigate it, not relearning fundamentals under a clock.

> Version note: CompTIA CySA+ moved to a new version, CS0-004, on June 23, 2026 — the older CS0-003 is being retired (English exam retiring December 22, 2026). This plan is built entirely around CS0-004. Confirm the version is still current at CompTIA.org before booking, since CompTIA revises on a roughly 3-year cycle.

---

## Gap Analysis

### Security+ (SY0-701) — 5 domains

| Domain                                    | Weight | My Status                                         | How This Plan Closes It                                   |
| ------------------------------------------ | ------ | -------------------------------------------------- | ----------------------------------------------------------- |
| 1. General Security Concepts               | 12%    | STRONG — covered by ISC2 CC                 | Week 1 rapid review only                                    |
| 2. Threats, Vulnerabilities, Mitigations    | 22%    | PARTIAL — conceptual, not scenario-tested    | Week 2-3: malware types, social engineering, PBQ practice   |
| 3. Security Architecture                   | 18%    | GAP — zero/hybrid cloud, segmentation, CASB | Week 4-5: network diagrams, cloud shared-responsibility lab |
| 4. Security Operations                     | 28%    | GAP — largest domain, log analysis, IR      | Week 5-7: SIEM lab, Windows Event Log review, PICERL drills |
| 5. Security Program Management & Oversight | 20%    | PARTIAL — governance overlap from ISC2 CC   | Week 7-8 review + full practice exams                       |

### CySA+ (CS0-004) — 4 domains

| Domain                            | Weight | My Status                                       | How This Plan Closes It                                          |
| ---------------------------------- | ------ | -------------------------------------------------- | --------------------------------------------------------------------- |
| 1. Security Operations              | 34%    | GAP — needs live SIEM reps, not just theory | Weeks 9-11: Splunk/Elastic queries, EDR/XDR concepts, AI-in-SOC risks |
| 2. Vulnerability Management         | 26%    | PARTIAL — Security+ scan lab overlaps       | Weeks 12-13: agent-based scanning, EPSS/CVSS prioritization           |
| 3. Incident Response & Management   | 24%    | PARTIAL — PICERL known from Security+       | Weeks 14-16: forensics depth, containment strategy scenarios         |
| 4. Reporting & Communication        | 16%    | GAP — never built a stakeholder report      | Week 17: KPI dashboards, exec summary writing                        |

### Blue Team Level 1 (BTL1) — 6 domains

| Domain                | My Status                                     | How This Plan Closes It                                     |
| ---------------------- | ------------------------------------------------ | ----------------------------------------------------------------- |
| Security Fundamentals  | STRONG by this point — Security+ + CySA+  | Skim only, Week 19                                              |
| Phishing Analysis       | GAP — no hands-on header/artifact analysis | Week 20: email header analysis, sandbox detonation             |
| Threat Intelligence     | PARTIAL — ATT&CK known, IOC lifecycle isn't | Week 21: MISP, IOC pivoting, TI report writing                 |
| Digital Forensics       | PARTIAL — order of volatility from Sec+     | Week 22: Autopsy, memory/disk artifacts, timeline building      |
| SIEM                    | STRONG by this point — CySA+ Splunk reps   | Week 23: BTL1-specific query patterns and case management       |
| Incident Response       | STRONG — PICERL drilled twice already      | Week 24: full simulated IR case, case management/reporting      |

### Detection Engineer (beyond all three certs)

| Requirement                          | My Status                                  | How This Plan Closes It                                            |
| ------------------------------------- | -------------------------------------------- | ---------------------------------------------------------------------- |
| Detection-as-code (Sigma rules)       | GAP — not started                    | Phase 2: sigma-detection-rules repo, version-controlled rules        |
| Adversary emulation / rule testing    | GAP — not started                    | Phase 4: Atomic Red Team against home SOC, validate detections fire   |
| Scripting for automation (Python)     | GAP — Bash only, no Python yet        | Phase 2-4: log parser + detection test harness in Python              |
| Documentation / runbook writing       | STRONG — 5 yrs staff training, rollout docs | Every lab write-up becomes a detection runbook, not just notes    |

### Shared Gaps (one project, multiple wins)

> Splunk/Elastic fluency built in Phase 2 (CySA+) is reused directly in BTL1's SIEM domain and the Phase 4 home SOC.
> PICERL, drilled first for Security+ Domain 4, gets applied at increasing depth in CySA+ Domain 3 and then tested for real in the BTL1 24-hour exam.
> Every Sigma rule and lab write-up compounds into the final home-soc-detection-lab capstone — nothing here is single-use study material.

---

## Milestone Overview

| Phase | Months | Focus                                          | Key Deliverable                                          | Cert / Tool                    |
| ----- | ------ | ------------------------------------------------- | ----------------------------------------------------------- | --------------------------------- |
| 1 | 1-2    | Security+ (SY0-701)                                | Domain 1-5 notes + exam passed                          | CompTIA Security+               |
| 2 | 3-5    | CySA+ (CS0-004) + detection-as-code                | Domain notes + exam passed + sigma-detection-rules repo | CompTIA CySA+, Splunk/Elastic  |
| 3 | 6-7    | Blue Team Level 1 (BTL1)                           | 6-domain notes + BTL1 practical exam passed             | BTL1 — Splunk, Wireshark, Autopsy |
| 4 | 8      | Home SOC capstone + apply                      | Full detection lab on GitHub + applications submitted       | Security Onion, Sysmon            |

---

## Phase 1 — Security+ (SY0-701), Months 1–2

> Focus: Fast review of what ISC2 CC already covered, then a full pass on the remaining four domains
> Target: ~28-35 hrs/month

### Week 1 — Domain 1 Review + Lab Setup

| Day | Activity                                                                                       | Time      |
| --- | ------------------------------------------------------------------------------------------------ | --------- |
| Mon | Download official SY0-701 exam objectives PDF from CompTIA.org — use as running checklist        | 1 hr      |
| Tue | Domain 1: CIA triad, AAA, zero trust, deception/disruption technology — Concept Cards for each   | 1.5 hr    |
| Wed | Domain 1: cryptographic concepts (symmetric/asymmetric, hashing, PKI basics)                     | 1.5 hr    |
| Thu | Domain 1: security control categories/types                                                      | 1 hr      |
| Fri | Set up VirtualBox + a Kali Linux VM and a Windows 10/11 VM — this becomes the study lab           | 1.5-2 hr  |

### Week 2 — Domain 2: Threats & Threat Actors

| Day | Activity                                                                                  | Time     |
| --- | -------------------------------------------------------------------------------------------- | -------- |
| Mon | Threat actor types and motivations                                                            | 1 hr     |
| Tue | Malware types deep dive: ransomware, worms, trojans, rootkits, fileless malware, botnets      | 1.5 hr   |
| Wed | Social engineering: phishing variants, pretexting, BEC, deepfakes — Concept Card each          | 1 hr     |
| Thu | Physical/network attacks: on-path, DoS/DDoS, DNS attacks, wireless attacks                    | 1.5 hr   |
| Fri | Practice questions: Domain 2 only, 20 questions, review every wrong answer                     | 1 hr     |

### Week 3 — Domain 2: Vulnerabilities & Mitigations

| Day | Activity                                                                                       | Time     |
| --- | ---------------------------------------------------------------------------------------------- | -------- |
| Mon | Vulnerability types: application, OS, web-based, cloud-specific, zero-day                       | 1 hr     |
| Tue | Vulnerability scanning concepts: false positive/negative, CVE/CVSS scoring practice              | 1.5 hr   |
| Wed | Mitigation techniques: segmentation, patching, hardening, compensating controls                  | 1 hr     |
| Thu | Hands-on: run Nmap and an OpenVAS/Nessus Essentials scan against lab VMs, read the report        | 1.5-2 hr |
| Fri | Write first lab debrief using the template                                                       | 1 hr     |

### Week 4 — Consolidation + Practice Exam #1

| Day | Activity                                                                     | Time   |
| --- | ------------------------------------------------------------------------------- | ------ |
| Mon | Review all Domain 1-2 Concept Cards — fill gaps                                | 1 hr   |
| Tue | Domain 1-2 practice exam (Professor Messer or CompTIA CertMaster free sample)    | 1.5 hr |
| Wed | Review every wrong answer, note the "why," not just the correct choice           | 1 hr   |
| Thu | Read one MITRE ATT&CK technique page per malware type covered this month        | 1 hr   |
| Fri | Weekly review + push notes to GitHub                                            | 1 hr   |

### Week 5 — Domain 3: Security Architecture

| Day | Activity                                                                              | Time     |
| --- | ---------------------------------------------------------------------------------------- | -------- |
| Mon | Network security design: segmentation, DMZ, zero trust architecture, east-west traffic    | 1.5 hr   |
| Tue | Cloud security: shared responsibility model, IaaS/PaaS/SaaS differences, CASB             | 1.5 hr   |
| Wed | Secure protocols: HTTPS, SSH, SFTP, LDAPS, TLS 1.3                                        | 1 hr     |
| Thu | Hands-on: create a free-tier AWS account, enable CloudTrail + GuardDuty, read findings     | 1.5 hr   |
| Fri | Infrastructure hardening: patch mgmt, config baselines, secure defaults                    | 1 hr     |

### Week 6 — Domain 4: Security Operations, Part 1

| Day | Activity                                                                                     | Time     |
| --- | ------------------------------------------------------------------------------------------------ | -------- |
| Mon | Identity and access management: federation, SSO, conditional access, PAM                          | 1 hr     |
| Tue | Endpoint security: EDR/XDR concepts, application allow-listing, host-based firewalls              | 1 hr     |
| Wed | Install Sysmon on the Windows lab VM with the SwiftOnSecurity config — read events                | 1.5-2 hr |
| Thu | Windows Security Event Log deep dive: 4624/4625/4688/4720                                        | 1.5 hr   |
| Fri | Practice questions: Domain 4 identity/endpoint sub-objectives                                     | 1 hr     |

### Week 7 — Domain 4 Part 2 + Domain 5

| Day | Activity                                                                                    | Time   |
| --- | ------------------------------------------------------------------------------------------- | ------ |
| Mon | Incident response lifecycle (PICERL) until the six phases are automatic                      | 1 hr   |
| Tue | Digital forensics basics: order of volatility, chain of custody, legal hold                  | 1 hr   |
| Wed | Domain 5: risk management, security policies, third-party risk, compliance frameworks        | 1.5 hr |
| Thu | Domain 5: security awareness training concepts, BC/DR                                        | 1 hr   |
| Fri | Full-length practice exam #2 (all 5 domains)                                                  | 1.5 hr |

### Week 8 — Exam Week

| Day | Activity                                                                       | Time   |
| --- | ---------------------------------------------------------------------------------- | ------ |
| Mon | Review every wrong answer from practice exam #2, focus on Domain 4 misses          | 1 hr   |
| Tue | PBQ-specific practice — log analysis scenarios                                     | 1 hr   |
| Wed | Light review only — flashcards, all domains                                       | 30 min |
| Thu | Book exam at Pearson VUE, ~1 week out; final full practice exam                    | 1.5 hr |
| Fri | Rest — light flashcard review only                                                 | 20 min |
| Sat | SIT COMPTIA SECURITY+ (SY0-701) EXAM                                        | —      |

### Phase 1 Goals

- [ ] CompTIA Security+ (SY0-701) certified
- [ ] Sysmon running on lab VM, events reviewed daily
- [ ] AWS free-tier account with CloudTrail + GuardDuty producing sample findings
- [ ] Security+ badge added to LinkedIn and resume

---

## Phase 2 — CySA+ (CS0-004), Months 3–5

> Focus: Move from Security+ vocabulary into applied SOC analyst skill — this is where detection engineering work formally begins
> Target: ~28-35 hrs/month, ~10 weeks

### Week 9 — Security Operations, Part 1: SIEM Fundamentals

| Day | Activity                                                                                          | Time     |
| --- | --------------------------------------------------------------------------------------------------- | -------- |
| Mon | Install Splunk Free (500MB/day) — ingest Sysmon logs from the Phase 1 lab VM                         | 1.5-2 hr |
| Tue | Write first 5 SPL queries: failed logons, process creation, new scheduled tasks                      | 1 hr     |
| Wed | MITRE ATT&CK Navigator — pick 5 techniques relevant to a Windows endpoint                              | 1 hr     |
| Thu | Map each Sysmon event type to the ATT&CK technique it can help detect                                 | 1 hr     |
| Fri | CS0-004 new content: AI in security operations — hallucinations, data exposure, model poisoning, prompt injection risk categories | 1 hr |

> CS0-004 explicitly tests AI risk categories that didn't exist in the prior version — don't skip this even though it feels less "technical" than SIEM work. It's tested content now.

### Week 10 — Security Operations, Part 2: Detection-as-Code Begins

| Day | Activity                                                                                       | Time   |
| --- | ---------------------------------------------------------------------------------------------- | ------ |
| Mon | Read the Sigma rule spec — start sigma-detection-rules repo                                    | 1 hr   |
| Tue | Write Rule 1: suspicious PowerShell encoded command (T1059.001)                                  | 1.5 hr |
| Wed | Write Rule 2: new scheduled task creation (T1053.005)                                            | 1 hr   |
| Thu | Convert both rules to SPL, run against Splunk lab data                                           | 1.5 hr |
| Fri | Document each rule: what it detects, false-positive conditions, tuning notes                     | 1 hr   |

### Week 11 — Security Operations, Part 3: Cloud & Zero Trust

| Day | Activity                                                                                | Time     |
| --- | ------------------------------------------------------------------------------------------ | -------- |
| Mon | Zero Trust and SASE basics as tested in CS0-004 architecture content                        | 1 hr     |
| Tue | Cloud-native monitoring: containers, APIs, hybrid cloud logging concepts                    | 1.5 hr   |
| Wed | Pull sample CloudTrail logs from the AWS lab account — write a detection for IAM policy changes | 1.5 hr |
| Thu | EDR/XDR platform concepts — how alerts correlate across host and network telemetry         | 1 hr     |
| Fri | Practice questions: Security Operations domain (34% weight — the biggest single investment)  | 1.5 hr   |

### Week 12 — Vulnerability Management, Part 1

| Day | Activity                                                                                  | Time   |
| --- | -------------------------------------------------------------------------------------------- | ------ |
| Mon | Agent-based vs. agentless scanning — when each is appropriate                                  | 1 hr   |
| Tue | CVSS v3.1/v4.0 scoring practice — score 5 sample CVEs by hand                                  | 1.5 hr |
| Wed | EPSS (Exploit Prediction Scoring System) — how it changes prioritization vs. CVSS alone        | 1 hr   |
| Thu | Cloud-native asset discovery concepts                                                          | 1 hr   |
| Fri | Run a second, more thorough vulnerability scan on the lab environment; prioritize findings by EPSS + CVSS | 1.5 hr |

### Week 13 — Vulnerability Management, Part 2

| Day | Activity                                                                       | Time   |
| --- | ----------------------------------------------------------------------------------- | ------ |
| Mon | Risk-based remediation planning — patch windows, compensating controls, exceptions   | 1 hr   |
| Tue | Write a Python script: parses a vulnerability scan export, flags anything above an EPSS/CVSS threshold | 1.5 hr |
| Wed | Practice questions: Vulnerability Management domain (26% weight)                    | 1.5 hr |
| Thu | Weekly review + push sigma-detection-rules progress to GitHub                     | 1 hr   |
| Fri | Concept Card: "CS0-003 vs CS0-004 — what actually changed and why it matters"       | 1 hr   |

### Week 14 — Incident Response & Management, Part 1

| Day | Activity                                                                          | Time   |
| --- | -------------------------------------------------------------------------------------- | ------ |
| Mon | PICERL revisited at CySA+ depth — containment strategies: isolation, segmentation, blocking | 1 hr   |
| Tue | Digital forensics fundamentals: evidence collection, chain of custody, write blockers  | 1.5 hr |
| Wed | Install Atomic Red Team on the lab VM                                                  | 1 hr   |
| Thu | Run one atomic test per existing Sigma rule — confirm the rule fires                   | 1.5 hr |
| Fri | For any rule that didn't fire, debug and tune it — document what was wrong             | 1 hr   |

### Week 15 — Incident Response & Management, Part 2

| Day | Activity                                                                                | Time   |
| --- | ---------------------------------------------------------------------------------------- | ------ |
| Mon | Script a small IR scenario using ATT&CK: phishing to BEC, or impossible travel to session theft | 1.5 hr |
| Tue | Walk the scenario through full PICERL, documenting each phase as if for a real ticket    | 1.5 hr |
| Wed | Write 2 more Sigma rules covering techniques not yet detected (credential access, persistence) | 1.5 hr |
| Thu | Spin up Elastic (Cloud trial or local ELK) — ingest the same Sysmon data, write equivalent detections in ES\|QL/KQL | 1.5 hr |
| Fri | Practice questions: Incident Response domain (24% weight)                                | 1 hr   |

### Week 16 — Incident Response Wrap-Up + Reporting Begins

| Day | Activity                                                                              | Time   |
| --- | -------------------------------------------------------------------------------------------- | ------ |
| Mon | Post-incident review concepts: root cause analysis, lessons learned documentation          | 1 hr   |
| Tue | Reporting domain: stakeholder-appropriate communication — executive vs. technical audiences | 1 hr   |
| Wed | Build a simple vulnerability dashboard with KPIs from the Week 12-13 scan data              | 1.5 hr |
| Thu | Write an executive summary and a technical incident report for the same simulated incident  | 1.5 hr |
| Fri | Practice questions: Reporting & Communication domain (16% weight)                           | 1 hr   |

### Week 17 — Full Practice Exams

| Day | Activity                                                                | Time   |
| --- | ---------------------------------------------------------------------------- | ------ |
| Mon | Full-length timed practice exam #1 (all 4 domains)                            | 1.5 hr |
| Tue | Review every wrong answer, note which domain needs more time                  | 1 hr   |
| Wed | Targeted review of weakest domain from Monday's exam                         | 1.5 hr |
| Thu | Full-length timed practice exam #2                                           | 1.5 hr |
| Fri | Push sigma-detection-rules polish + weekly review                          | 1 hr   |

### Week 18 — Exam Week

| Day | Activity                                                                    | Time   |
| --- | -------------------------------------------------------------------------------- | ------ |
| Mon | Review wrong answers from practice exam #2                                       | 1 hr   |
| Tue | Book exam at Pearson VUE, ~1 week out                                             | 15 min |
| Wed | PBQ-specific practice — log analysis, scan interpretation, IR step sequencing     | 1.5 hr |
| Thu | Light review — flashcards on AI risk categories and EPSS/CVSS distinctions        | 45 min |
| Fri | Rest — no new material                                                            | —      |
| Sat | SIT COMPTIA CYSA+ (CS0-004) EXAM                                          | —      |

### Phase 2 Goals

- [ ] CompTIA CySA+ (CS0-004) certified
- [ ] sigma-detection-rules repo published: at least 6 detections, each tested with Atomic Red Team, each documented with false-positive notes
- [ ] Splunk and Elastic both ingesting lab log data
- [ ] Python vulnerability-triage script written and working
- [ ] One full simulated incident walked through PICERL with both an executive and technical report written

---

## Phase 3 — Blue Team Level 1 (BTL1), Months 6–7

> Focus: Prove the skills hands-on — no multiple choice, a real 24-hour investigation
> Target: ~20-30 hrs/month; official estimate is 30-50 hrs of study for candidates with a security background, which this plan comfortably exceeds by this point

### Week 19 — Purchase + Security Fundamentals

| Day | Activity                                                                                      | Time   |
| --- | ------------------------------------------------------------------------------------------------ | ------ |
| Mon | Purchase BTL1 (~£399/$490, includes 100 hrs labs, 4 months training access, 12 months to exam, 2 attempts) | 30 min |
| Tue | Security Fundamentals domain — mostly review at this point; skim and note any BTL1-specific terminology | 1 hr   |
| Wed | Complete the free Blue Team Junior Analyst (BTJA) pathway modules as a self-assessment              | 1.5 hr |
| Thu | Start BTL1 labs — get comfortable with the in-browser lab environment and its copy/paste limitations | 1 hr   |
| Fri | Weekly review                                                                                        | 1 hr   |

### Week 20 — Phishing Analysis

| Day | Activity                                                                          | Time   |
| --- | ---------------------------------------------------------------------------------------- | ------ |
| Mon | Email header analysis: SPF, DKIM, DMARC, spoofing indicators                              | 1.5 hr |
| Tue | BTL1 phishing labs — analyze headers and identify spoofed senders                          | 1.5 hr |
| Wed | Sandbox detonation concepts — safely analyzing a suspicious attachment/URL                 | 1 hr   |
| Thu | BTL1 phishing labs — attachment and URL analysis                                          | 1.5 hr |
| Fri | Write a Concept Card: "How I'd triage a reported phishing email end-to-end"               | 1 hr   |

### Week 21 — Threat Intelligence

| Day | Activity                                                                    | Time   |
| --- | ---------------------------------------------------------------------------------- | ------ |
| Mon | IOC lifecycle: collection, validation, sharing, aging out stale indicators           | 1 hr   |
| Tue | Set up MISP — practice curating and pivoting on IOCs                                | 1.5 hr |
| Wed | BTL1 threat intel labs                                                              | 1.5 hr |
| Thu | Write a short threat intelligence report from a sample IOC set, BTL1 report format  | 1.5 hr |
| Fri | Practice questions/labs review                                                      | 1 hr   |

### Week 22 — Digital Forensics

| Day | Activity                                                                | Time   |
| --- | ------------------------------------------------------------------------------ | ------ |
| Mon | Install and explore Autopsy — disk image analysis basics                        | 1.5 hr |
| Tue | Memory forensics concepts — what lives in RAM that disk imaging misses          | 1 hr   |
| Wed | BTL1 forensics labs — timeline building from artifacts                          | 1.5 hr |
| Thu | BTL1 forensics labs — continue, focus on Windows artifact locations             | 1.5 hr |
| Fri | Weekly review                                                                    | 1 hr   |

### Week 23 — SIEM (BTL1-Specific Practice)

| Day | Activity                                                                | Time   |
| --- | ------------------------------------------------------------------------------ | ------ |
| Mon | BTL1 SIEM labs using Splunk — this should feel largely familiar from Phase 2   | 1.5 hr |
| Tue | Practice BTL1's specific query and case-management conventions                 | 1.5 hr |
| Wed | Wireshark refresh — filters relevant to the BTL1 exam scenarios                | 1 hr   |
| Thu | DeepBlueCLI — Windows Event Log triage tool used in the BTL1 exam              | 1 hr   |
| Fri | Weekly review                                                                    | 1 hr   |

### Week 24 — Incident Response + Full Practice Case

| Day | Activity                                                                       | Time   |
| --- | ------------------------------------------------------------------------------------ | ------ |
| Mon | TheHive — case management concepts used in the BTL1 IR domain                        | 1 hr   |
| Tue | Walk a full simulated IR case start to finish using Splunk + Wireshark + Autopsy      | 2 hr   |
| Wed | Write the case up in BTL1's expected reporting format: scope, findings, recommendations | 1.5 hr |
| Thu | Review weakest domain based on lab performance so far                                | 1.5 hr |
| Fri | Build a consolidated notes document, organized by domain — this is your open-book reference during the exam | 1.5 hr |

### Week 25 — Final Prep

| Day | Activity                                                                    | Time   |
| --- | ---------------------------------------------------------------------------------- | ------ |
| Mon | Finish any remaining labs from the 100-hour lab library                             | 1.5 hr |
| Tue | Rehearse tool workflows without notes: Splunk search, Wireshark filter, Autopsy triage | 1.5 hr |
| Wed | Review and organize the consolidated notes doc — index it for fast lookup            | 1 hr   |
| Thu | Rest / light review only                                                            | 30 min |
| Fri | Confirm exam environment access, block out a full 24-hour window on the calendar     | 15 min |

### Week 26 — Exam

| Day       | Activity                                                                                                  | Time   |
| --------- | ------------------------------------------------------------------------------------------------------------- | ------ |
| Sat/Sun   | SIT THE BTL1 24-HOUR PRACTICAL EXAM — open-book, unproctored, 20 task-based challenges, aim for 70%+ (90%+ earns the gold coin) | 24 hr  |

> AI tools (ChatGPT, etc.) are explicitly prohibited during the BTL1 exam and will result in disqualification — the point of the exam is demonstrating your own investigative process.

### Phase 3 Goals

- [ ] Blue Team Level 1 (BTL1) certified
- [ ] Consolidated, indexed notes document built and battle-tested
- [ ] Comfortable investigating a live incident across Splunk, Wireshark, Autopsy, and DeepBlueCLI without hesitation
- [ ] BTL1 badge/coin added to LinkedIn and resume

---

## Phase 4 — Home SOC Capstone + Apply, Month 8

> Focus: Ship one cohesive detection lab as the portfolio centerpiece, then apply
> Target: ~28-35 hrs this month

### Week 27 — Build the Home SOC

| Day | Activity                                                                                       | Time     |
| --- | --------------------------------------------------------------------------------------------------- | -------- |
| Mon | Deploy Security Onion (or keep the Elastic stack) as the central log/detection platform on ZimaBoard | 2 hr     |
| Tue | Forward Sysmon + Windows Event Logs from the lab VM into the SOC platform                            | 1.5 hr   |
| Wed | Forward AWS CloudTrail/GuardDuty findings into the same platform                                     | 1.5 hr   |
| Thu | Import all sigma-detection-rules detections into the SOC platform's rule engine                    | 1.5 hr   |
| Fri | Full end-to-end test: run Atomic Red Team, confirm alerts appear in the SOC dashboard                | 1.5 hr   |

### Week 28 — Expand Detection Coverage

| Day | Activity                                                                                | Time   |
| --- | -------------------------------------------------------------------------------------------- | ------ |
| Mon | Add 3 more detections covering lateral movement techniques (T1021 family)                     | 1.5 hr |
| Tue | Add detection for data exfiltration over common ports (T1041/T1048)                            | 1.5 hr |
| Wed | Build a dashboard: alert volume by technique, top noisy rules — reuse Phase 2 reporting skills | 1.5 hr |
| Thu | Write an incident report for one simulated attack chain end-to-end (PICERL structure)          | 1.5 hr |
| Fri | Track and log one "what broke" incident from the SOC build itself                              | 1 hr   |

### Week 29 — Document Everything

| Day | Activity                                                                          | Time   |
| --- | -------------------------------------------------------------------------------------- | ------ |
| Mon | Write the capstone README: architecture diagram, data flow, design decisions           | 1.5 hr |
| Tue | Write a runbook: how to onboard a new log source and write its first detection       | 1.5 hr |
| Wed | Write the post-incident report from the simulated attack chain in full                | 1.5 hr |
| Thu | Pin the capstone repo as featured on GitHub                                            | 1 hr   |
| Fri | Add capstone to LinkedIn as a Featured project with a short write-up                   | 1 hr   |

### Week 30 — Resume + Applications

| Day | Activity                                                                                                | Time   |
| --- | ---------------------------------------------------------------------------------------------------------- | ------ |
| Mon | Resume review — three certs (Security+, CySA+, BTL1) plus ISC2 CC, tailored to Detection Engineer postings  | 1 hr   |
| Tue | Cover letter — lead with the SOC capstone and the cert progression as evidence of sustained focus           | 1 hr   |
| Wed | Technical prep: walk me through a detection you wrote and how you validated it                            | 1.5 hr |
| Thu | Technical prep: walk me through your BTL1 exam investigation + how would you triage this alert          | 1 hr   |
| Fri | Submit applications — resume + cover letter + GitHub link                                                | 1 hr   |

### Phase 4 Goals

- [ ] Home SOC running on ZimaBoard, ingesting endpoint, Windows, and cloud logs
- [ ] 10+ detections deployed, each validated against Atomic Red Team
- [ ] One full incident report written end-to-end, PICERL-structured
- [ ] home-soc-detection-lab repo published as the featured portfolio piece
- [ ] Detection Engineer and SOC Analyst applications submitted
- [ ] 7-month roadmap complete, three certifications earned

---

## Homelab SOC Projects

> Hardware: ZimaBoard 832 (Intel Celeron, 8GB RAM, dual SATA, dual GbE)

| # | Project                                                       | Phase | Relevance                                        |
| - | -------------------------------------------------------------- | ----- | ---------------------------------------------------- |
| 1 | Vulnerability scan of lab VMs (Nmap + OpenVAS/Nessus)          | 1     | Security+ Domain 2, first EPSS/CVSS practice          |
| 2 | Sysmon deployment + Windows Event Log analysis                | 1-2   | Core endpoint telemetry every later phase builds on   |
| 3 | AWS CloudTrail + GuardDuty sample findings review              | 1-2   | Cloud log source, Security+/CySA+ overlap             |
| 4 | Sigma detection rules, tested against Atomic Red Team          | 2     | Direct detection-engineering evidence             |
| 5 | Simulated IR case walked through PICERL with dual reporting    | 2-3   | CySA+ Reporting domain + BTL1 case management practice |
| 6 | Home SOC (Security Onion/Elastic) with all sources centralized | 4     | Capstone — the whole job in one repo              |

### Write-Up Structure (use for all projects)

```
## Problem Statement
What you were trying to detect or understand, and why

## Data Sources
What logs/telemetry feed this — host, network, cloud

## What I Did
Step by step — include the queries/rules that mattered

## Validation
How you proved the detection works — Atomic Red Team test, sample data, etc.

## False Positives / Tuning
What triggered incorrectly and how you narrowed it

## What I'd Do Differently
Shows engineering maturity

## ATT&CK Mapping
Technique ID(s) this detection or finding maps to
```

---

## Resources & Links

### Official / Structured

| Resource                                                  | Use                          | Phase |
| ------------------------------------------------------------ | -------------------------------- | ----- |
| CompTIA SY0-701 official exam objectives (CompTIA.org)        | Security+ syllabus, verify version | 1     |
| Professor Messer SY0-701 free video course                    | Security+ domain walkthrough      | 1     |
| CompTIA official CS0-004 exam objectives (CompTIA.org)         | CySA+ syllabus — confirm V4, not V3 | 2     |
| CompTIA CertMaster free practice questions                    | Practice exams, both certs        | 1-2   |
| Security Blue Team official BTL1 course + labs                | BTL1 primary training source      | 3     |
| Blue Team Junior Analyst (BTJA) free pathway                  | Free self-assessment before BTL1  | 3     |

### Free Hands-On Resources

| Resource                                        | What For                                  | Phase |
| -------------------------------------------------- | ---------------------------------------------- | ----- |
| VirtualBox                                          | Local Kali + Windows lab VMs                  | 1     |
| OpenVAS / Nessus Essentials (free tier)             | Vulnerability scanning                        | 1-2   |
| SwiftOnSecurity Sysmon config (GitHub)               | Production-quality Sysmon baseline            | 1     |
| AWS Free Tier                                       | CloudTrail + GuardDuty sample findings        | 1-4   |
| Splunk Free (500MB/day)                             | SIEM query practice                           | 2-3   |
| Elastic Cloud free trial / local ELK                | Second SIEM, ES\|QL/KQL practice              | 2     |
| MITRE ATT&CK Navigator                               | Technique mapping                             | 2-4   |
| Sigma rule spec + pySigma                          | Detection-as-code format and conversion        | 2     |
| Atomic Red Team                                     | Adversary emulation to validate detections     | 2, 4  |
| MISP                                                 | Threat intel IOC curation and pivoting         | 3     |
| Autopsy                                              | Digital forensics — disk/timeline analysis     | 3     |
| Wireshark                                            | Packet analysis                                | 3     |
| DeepBlueCLI                                          | Windows Event Log triage                       | 3     |
| TheHive                                              | Case management concepts                       | 3     |
| Security Onion                                       | Free, purpose-built SOC platform              | 4     |

### Paid Resources

| Resource                                    | Cost         | What For                    | Phase |
| ---------------------------------------------- | ------------ | ---------------------------- | ------ |
| CompTIA Security+ exam voucher                 | ~$404-425    | The Security+ exam            | End Phase 1 |
| CompTIA CySA+ (CS0-004) exam voucher            | ~$404-425    | The CySA+ exam                | End Phase 2 |
| Blue Team Level 1 training + exam bundle        | ~£399 GBP / ~$490 USD | BTL1 training, labs, and 2 exam attempts | Start of Phase 3 |

> Confirm current active exam versions and pricing at CompTIA.org and securityblue.team before registering or purchasing — both CompTIA exams revise on a roughly 3-year cycle, and BTL1 content is periodically refreshed.

---

## GitHub Portfolio — Target State by Phase 4

| Repo                        | Purpose                                                             | Closes Gap For                             |
| ---------------------------- | ---------------------------------------------------------------------- | --------------------------------------------- |
| secplus-detection-notes    | This vault — domain notes, concept cards, weekly reviews                | Interview credibility, study discipline       |
| sigma-detection-rules      | Version-controlled Sigma rules, each tested and documented              | Detection-as-code, ATT&CK fluency             |
| home-soc-detection-lab     | Full SOC build: Security Onion/Elastic + all log sources + dashboard   | Capstone — end-to-end detection engineering  |

---

## Note-Taking Templates

### Concept Card

```
---
date:
topic:
tags:
source:
---

# Concept:

## What it is
(Plain English — one paragraph max)

## How it works
(The mechanism — what actually happens under the hood)

## Real-world example
(How this shows up in an actual attack or a real SOC environment)

## ATT&CK mapping (if applicable)
(Technique ID)

## Related concepts
-

## Questions I still have
-
```

### Lab Debrief

```
---
date:
platform:
tags:
---

# Lab:

## Objective

## Environment
- Hardware: ZimaBoard 832 / AWS Free Tier / Local VM
- Log sources:
- Tools used:

## What I did
1.
2.
3.

## What broke and how I fixed it
(Mandatory — always write something here)

## Detections validated / queries used

## What I'd do differently

## How this maps to a Detection Engineer role
```

### Weekly Review

```markdown
---
date:
week:
tags: weekly-review
---

# Week __ Review

## Hours studied
Target: 5-10 hrs  |  Actual:

## Topics covered

## Biggest thing I learned this week

## What confused me

## How I resolved it (or plan to)

## Detections written / labs run this week

## Practice exam or test score
This week: __%  |  Last week: __%  |  Trend: up / down / flat

## Energy and motivation (1-10)

## One thing to do differently next week
```

### Incident Report

```markdown
---
date:
scenario:
tags: incident-report
---

# Incident Report:

## Scope
What systems/data were involved

## Timeline
Chronological sequence of events, timestamped

## Findings
What the investigation uncovered

## Root Cause

## Containment / Remediation Actions Taken

## Recommendations
Stakeholder-facing, prioritized

## Lessons Learned
```

---

## Application Strategy

### Wave 1 — End of Phase 2 (After CySA+)

Apply to SOC Analyst Tier 1/2 roles once CySA+ is earned. At that point the resume has:

- Security+ and CySA+ back to back, plus ISC2 CC
- sigma-detection-rules repo live with tested, documented detections
- 5+ years production infrastructure experience
- 5 months of consistent GitHub commits

### Wave 2 — End of Phase 4 (Strongest Application Window)

By this point: all three certifications earned, sigma-detection-rules and home-soc-detection-lab both published, 10+ validated detections, a full incident report, and eight months of consistent GitHub activity. This is the strongest window for Detection Engineer specifically — most entry-level postings in this space explicitly look for a home lab or personal detection project, and by Phase 4 that exists as a complete, three-cert-backed artifact.

### Target Roles

- Detection Engineer (primary)
- SOC Analyst Tier 1/2 (primary — leverages ISC2 CC + Security+ + CySA+ directly)
- Security Analyst
- Threat Detection Analyst / Content Engineer (SIEM-vendor specific roles)
- Junior Security Engineer / Incident Responder

---

## Daily Study Habit

After every session, commit your notes:

```
cd ~/secplus-detection-notes
git add .
git commit -m "Notes: [topic] — $(date +%Y-%m-%d)"
git push origin main
```

Examples:

```
Notes: Domain 4 IR lifecycle (PICERL) — 2026-09-02
Lab: Sysmon deployment on Windows VM — 2026-09-08
Rule: Sigma detection for encoded PowerShell — 2026-09-22
Notes: CS0-004 AI risk categories — 2026-10-06
Lab: BTL1 phishing header analysis — 2026-12-08
Review: Week 9 — 2026-09-05
```

---

> The ISC2 CC and five years of infrastructure work are not a blank slate — they're a head start most Security+ candidates don't have. Three certifications in seven months at 5-10 hours a week is a real commitment, but each one hands off directly to the next: Security+ gives the vocabulary, CySA+ gives the applied SOC skill, and BTL1 proves it under a clock with no multiple-choice safety net. By Phase 4 the actual deliverable isn't a stack of certificates — it's a working detection lab that answers "show me something you built" with an artifact instead of a sentence.

---

*Last updated: July 2026*
