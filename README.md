<div align="center">

# Ram Badhiwala
### SOC Analyst II · Threat Detection & Response · Detection Engineering · SOAR Automation

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/rambadhiwala)
[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:rambadh42@gmail.com)
[![CompTIA CySA+](https://img.shields.io/badge/CompTIA-CySA%2B-red?style=for-the-badge&logo=comptia&logoColor=white)](https://www.comptia.org/)
[![SC-200](https://img.shields.io/badge/Microsoft-SC--200%20In%20Progress-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)](https://learn.microsoft.com/en-us/credentials/certifications/security-operations-analyst/)

</div>

---

## 👨‍💻 About Me

SOC Analyst with **4 years of enterprise experience** at Cisco, Capital One, and HCL Technologies. I work across the full Tier 1/2 lifecycle — monitoring, triage, detection engineering, incident response, and SOAR automation — with a strong focus on reducing noise and improving containment speed.

- 🔍 Monitoring ~3,500 daily security events across Splunk, Microsoft Sentinel, and CrowdStrike Falcon
- ⚡ Reduced MTTD by 18% and false positive rate by 22% through improved detection logic and RCA
- 🛡️ 94% containment rate across 40+ systems via endpoint isolation and SOAR-driven response
- 🤖 Built Python + Cortex XSOAR playbooks saving ~6 analyst hours per week
- 🎓 M.S. Cybersecurity — UNC Charlotte (May 2025) | CompTIA CySA+ | SC-200 In Progress

---

## 🛠️ Tech Stack

| Category | Tools |
|---|---|
| **SIEM** | Splunk (SPL), Microsoft Sentinel (KQL), IBM QRadar, LogRhythm, Rapid7 InsightIDR, AlienVault |
| **EDR** | CrowdStrike Falcon, SentinelOne, Microsoft Defender, Cortex XSIAM, OSSEC |
| **SOAR & Automation** | Cortex XSOAR, Python, PowerShell, Playbook Development |
| **Detection Engineering** | Sigma, Splunk SPL, KQL, Elastic EQL, MITRE ATT&CK Mapping |
| **Incident Response** | Alert Triage, IOC Analysis, Sandbox Detonation, RCA, Endpoint Isolation |
| **Cloud Security** | AWS CloudTrail, Azure Activity Logs, IAM, API Security, Active Directory |
| **Network** | TCP/IP, DNS, IDS/IPS, Wireshark, Snort, Suricata |
| **Frameworks** | MITRE ATT&CK, Cyber Kill Chain, NIST 800-61, NIST 800-53, ISO 27001, PCI-DSS |

---

## 🚀 Projects

### 🛡️ [Ransomware Canary Defense](https://github.com/rambadhiwala/Ransomware-Canary-Defense)
`Python` `HIDS` `SOAR` `File Integrity Monitoring`

A Python-based Host Intrusion Detection System (HIDS) using a **honeytoken architecture** to detect ransomware encryption attempts in real time. Deploys hidden bait files (financial docs, password lists) as tripwires, monitors them with the `watchdog` library, and triggers automated response in under 10ms.

**Key engineering detail:** Solved a race condition where the network kill switch executed faster than the SOC alert could transmit — refactored to enforce synchronous alert delivery before host isolation, guaranteeing 100% alert reliability.

- `generate_canaries.py` — Creates hidden bait directory with high-value decoy files
- `ransomware_monitor.py` — Real-time FIM agent + response orchestrator
- `restore_network.py` — Post-incident network re-enablement script
- Dispatches SOAR alerts to Discord/Slack webhook on trigger
- Maps to MITRE ATT&CK T1486 (Data Encrypted for Impact)

---

### 📚 [SOC Detection & Investigation Library](https://github.com/rambadhiwala/soc-detection-investigation-library)
`Splunk SPL` `Microsoft Sentinel KQL` `Sigma` `MITRE ATT&CK`

A comprehensive Tier 1/2 SOC portfolio covering detections, triage playbooks, complete case write-ups, and operational docs — built around real SOC workflows.

**Detection coverage** (each with SPL + KQL + Sigma formats, MITRE mapping, false positive tuning, and triage notes):
- Auth & Identity: brute force, password spray, impossible travel, MFA fatigue, new admin assignment
- Email & M365: phishing link, suspicious attachment, auto-forwarding rule, OAuth consent risk
- Endpoint: encoded PowerShell, Office spawning PowerShell, LOLBins
- Cloud & DLP/Exfil: SharePoint/OneDrive mass download, external sharing spike, DLP rule match

**Playbooks** (`/playbooks`): Phishing, Suspicious Login, Password Spray, MFA Fatigue, Email Forwarding Rules, Suspicious PowerShell, Mass Download, DLP Alert — each with escalation handoff and comms templates.

**Casebook** (`/casebook`): 10 complete written cases, each documented with `case-summary`, `timeline`, `triage-notes`, `evidence`, `decision`, `escalation`, and `lessons-learned` files — written the way real SOC tickets read.

---

### 🔬 [SIEM Detection Engineering & Investigation Workflows](https://github.com/rambadhiwala/siem-detection)
`Sigma` `Splunk SPL` `KQL` `Elastic EQL` `Python`

A multi-platform detection engineering repository using **Sigma as the source of truth**, with conversion to Splunk SPL, Microsoft Sentinel KQL, and Elastic EQL. Paired with step-by-step investigation playbooks and MITRE ATT&CK severity scoring.

```
detections/sigma/     # Platform-agnostic rules (convert to any SIEM)
detections/splunk/    # SPL searches + tuning notes
detections/kql/       # Sentinel KQL queries
detections/elastic/   # EQL examples
workflows/            # Triage → scoping → containment → closure playbooks
templates/            # Case notes, evidence capture, incident reporting
scripts/              # Validation helpers and index scripts
data/                 # Synthetic log samples for demos
```

---

### 🎣 [SOC Alert Triage & Phishing Investigation Lab](https://github.com/rambadhiwala/soc-alert-triage-phishing)
`Splunk SPL` `Microsoft Sentinel KQL` `Email Header Analysis` `IOC Validation`

A Tier-1 SOC simulation for phishing alert triage — from initial alert through evidence collection, true/false positive decision, and escalation. Includes investigations, playbooks, SPL/KQL queries, and synthetic sample data.

---

### 📋 [Alert Triage Playbooks](https://github.com/rambadhiwala/Alert-Triage-Playbook)
`SOC Operations` `Incident Response` `Banking & Enterprise`

Day-to-day SOC triage playbooks built for banking and enterprise environments, covering step-by-step triage flows, evidence collection checklists, escalation criteria, and containment actions.

- `Phishing_Alert_Playbook.md`
- `Malware_Detection_Playbook.md`
- `Suspicious_Login_Playbook.md`
- `DLP_Alert_Playbook.md` *(banking-focused)*

---

### 🔎 [Incident Escalation Case Studies](https://github.com/rambadhiwala/Incident-Escalation-CaseStudies)
`Tier 1 → Tier 2 Escalation` `NIST 800-61` `Incident Documentation`

Real-world SOC escalation workflows showing what Tier 1 handled, why escalation was required, and how Tier 2 investigated — with clean escalation handoff notes and reusable templates.

- Case 01: Malware Detection → Tier 2 Escalation
- Case 02: Credential Compromise Investigation
- Case 03: Suspicious Login from Foreign IP
- `/Templates`: Reusable escalation handoff and documentation templates

---

## 📊 Career Metrics

| Metric | Result |
|---|---|
| Daily Events Monitored | ~3,500 (Cisco) |
| MTTD Improvement | ↓ 18% |
| Avg. Investigation Turnaround | 42 min → 35 min |
| False Positive Rate Reduction | ↓ 22% (Cisco) · ↓ 17% (Capital One) |
| Containment Rate | 94% across 40+ systems |
| SOAR Time Savings | ~6 analyst hours/week |
| Incident Closure Rate | >95% (HCL, 30+ client environments) |

---

## 📈 GitHub Stats

<div align="center">

![Ram's GitHub Stats](https://github-readme-stats.vercel.app/api?username=rambadhiwala&show_icons=true&theme=github_dark&hide_border=true&include_all_commits=true&count_private=true)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=rambadhiwala&layout=compact&theme=github_dark&hide_border=true)

</div>

---

<div align="center">
<i>Building tools that detect faster, contain smarter, and document clearly.</i>
</div>
