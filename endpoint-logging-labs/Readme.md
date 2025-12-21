# 🔬 SOC LABS — Linux & Windows Logging and Investigation

## 📌 Overview
This repository contains **hands-on SOC labs** focused on detecting, investigating, and reconstructing attacker activity using **native operating system logs** from both **Linux and Windows environments**.

The labs simulate real-world attacker behavior and demonstrate how a SOC analyst can perform **end-to-end investigations** using built-in logging sources only — without SIEMs or third-party security tools.

The primary focus is on **context, correlation, and timeline reconstruction**, which are critical SOC investigation skills.

---

## 🎯 Objectives
- Understand where security-relevant logs exist on Linux and Windows
- Detect authentication abuse and brute-force attempts
- Identify privilege escalation activity
- Detect persistence mechanisms
- Correlate events across multiple log sources
- Reconstruct attacker timelines accurately
- Build SOC-ready investigation methodology

---

## 🧱 Lab Environments

### 🐧 Linux Environment
- **Victim:** Ubuntu Server
- **Attacker:** Kali Linux / Windows 11
- **Access Method:** SSH

**Primary Log Sources**
- `/var/log/auth.log`
- `/var/log/syslog`
- `journalctl`

---

### 🪟 Windows Environment
- **Operating System:** Windows 10 / Windows 11
- **Telemetry:** Windows Security Logs + Sysmon
- **Tools:** Event Viewer, Sysmon (Sysinternals)

**Primary Log Sources**
- Windows Event Viewer → Security
- Sysmon Operational Logs

---

## 🐧 Linux SOC Labs (Ubuntu Server + Kali)

### Covered Topics
- SSH failed login attempts
- SSH successful authentication
- Privilege escalation via sudo
- Failed sudo attempts
- Cron job creation (persistence)
- Log correlation using journalctl
- Log rotation awareness
- Timeline reconstruction

### Key Linux Logs
| Log Source | Purpose |
|----------|--------|
| `/var/log/auth.log` | SSH authentication & sudo activity |
| `/var/log/syslog` | Cron jobs & system activity |
| `journalctl` | Structured correlation & timelines |

### Linux SOC Focus
- Initial access via SSH
- Privilege escalation detection
- Persistence via cron
- Event sequencing across logs
- Awareness of rotated logs during investigations

---

## 🪟 Windows SOC Labs (Windows Security Logs + Sysmon)

### Covered Topics
- Successful and failed logons (4624 / 4625)
- Privileged logons (4672)
- Process creation (4688)
- Elevated process detection
- Sysmon process telemetry (Event ID 1)
- Network connections (Sysmon Event ID 3 / 22)
- File creation events (Sysmon Event ID 11)

### Key Windows Event IDs
| Event ID | Description |
|--------|------------|
| 4624 | Successful logon |
| 4625 | Failed logon |
| 4688 | Process creation |
| 4672 | Special privileges assigned |
| 1102 | Security log cleared |
| Sysmon 1 | Process creation |
| Sysmon 3 | Network connection |
| Sysmon 11 | File creation |

### Windows SOC Focus
- Authentication vs privilege separation
- Elevated activity detection
- Process lineage analysis
- Process → network → file correlation
- Noise reduction using Sysmon telemetry

---

## 🕵️ SOC Investigation Methodology
Across both platforms, the labs emphasize:

- Context over isolated log entries
- Frequency and repetition analysis
- User and privilege tracking
- Source IP and process correlation
- Accurate timestamp alignment
- Full attack lifecycle reconstruction:
  - Initial Access
  - Privilege Escalation
  - Persistence

---

## 📊 Key Outcomes
By completing these labs, a SOC analyst can:
- Confidently navigate Linux and Windows logs
- Detect common attacker techniques
- Correlate events across multiple log sources
- Reconstruct accurate incident timelines
- Investigate incidents using **native OS logs only**

---

## 🧠 Core SOC Takeaway
> Effective security investigations rely on **correlation, context, and chronological sequencing**, not on single log entries or standalone Event IDs.

