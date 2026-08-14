# 14 — Homelab SOC

Build notes for the ZimaBoard-hosted SOC platform (Security Onion/Elastic),
Sysmon deployment, and log flow — this folder documents the Phase 4 capstone
as it's built. The finished, presentable version lives in its own
`home-soc-detection-lab` repo.

## Build Checklist
- [ ] Security Onion (or Elastic stack) deployed on ZimaBoard
- [ ] Sysmon + Windows Event Logs forwarded in
- [ ] AWS CloudTrail/GuardDuty findings forwarded in
- [ ] All `sigma-detection-rules` imported into the rule engine
- [ ] Atomic Red Team end-to-end validation run
- [ ] Dashboard built: alert volume by technique, top noisy rules
