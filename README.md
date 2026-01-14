# 🛡️ SOC Fundamentals Labs

> Hands-on SOC labs focused on **attacker behavior**, **network & host visibility**, and **real analyst workflows**.  
> Built to prove **how I think as a SOC analyst**, not what tools I can click.

This repository demonstrates **practical SOC capability** through controlled labs covering **networking, endpoint logging, SIEM foundations, and identity telemetry**.

This is **not certification prep**.  
This is **evidence of analyst thinking**.

---

## 🔍 What This Repository Proves

✔ Core **SOC L1 fundamentals**  
✔ Understanding of **network, firewall, endpoint, and identity behavior**  
✔ Ability to **differentiate normal vs suspicious activity**  
✔ Skill in **correlating attacker, victim, endpoint, and SIEM evidence**  
✔ Analyst reasoning **beyond alerts, dashboards, and signatures**

This is **not a tutorial dump**.  
This is **proof of hands-on SOC investigation skills**.

---

## 🧠 Core Philosophy

> **Logs are evidence — not decorations.**  
> If log generation is wrong, detection is impossible.

This repository prioritizes:
- Correct **log generation** before ingestion
- Clean **signal over noise**
- Logical **data separation**
- Evidence-driven **validation**
- SOC reasoning before automation

---

## 🧪 Lab Environment

| Component | Role |
|--------|------|
| Kali Linux | Attacker / scanning / probing |
| Ubuntu Server | SIEM, firewall, logging, control point |
| Windows 11 | Enterprise endpoint / user activity |
| Windows 10 | Endpoint telemetry |
| Windows Server 2019 | Active Directory / identity authority |
| Network | Host-only + NAT (isolated lab) |

All activity is **fully controlled and observable**.

---

## 📂 Repository Structure

soc-fundamentals-labs/
│
├── SOC-SIEM-Learning/
│ ├── Foundations/
│ └── SIEM_Setup/
│ ├── SOC SIEM LAB-SETUP.docx
│ ├── SPLUNK ENTERPRISE SETUP AND LINUX LOG INGESTION.docx
│ ├── SPLUNK FORWARDER SETUP & WINDOWS 10 ENDPOINT LOG INGESTION.docx
│ └── SPLUNK FORWARDER SETUP & WINDOWS SERVER 2019 (AD).docx
│
├── networking/
├── network-traffic-analysis/
├── endpoint-logging-labs/
└── README.md


---

## 🧪 Lab Categories

---

### 🌐 Networking Fundamentals  
📁 `networking/`

**Skills covered**
- TCP/IP 3-way handshake (packet-level understanding)
- Ports vs protocols (common SOC misconception)
- Trusted port abuse (443 ≠ HTTPS)
- Netcat usage (C2-style communication)

Each lab includes:
- 🎯 Objective  
- 🧱 Lab setup  
- ⚙️ Commands executed  
- 👀 Observations  
- 🧠 SOC takeaway  
- 🚨 Detection angle  

---

### 🌐 Network Traffic Analysis  
📁 `network-traffic-analysis/`

Focuses on **DNS, HTTP, and firewall traffic** with emphasis on **behavioral patterns and visibility boundaries**.

**Skills covered**
- DNS resolution and abuse
- HTTP behavior and beaconing indicators
- Firewall ALLOW vs BLOCK interpretation
- Inbound vs outbound traffic analysis
- SRC / DST / SPT / DPT field analysis
- Visibility gaps (what firewalls can and cannot see)

Includes **attacker + firewall + endpoint correlation labs**.

---

### 🖥️ Endpoint Logging & System Behavior  
📁 `endpoint-logging-labs/`

Focuses on **host-level visibility**.

**Skills covered**
- Windows authentication and process activity
- Linux authentication and service logs
- Differentiating system noise from attacker behavior
- Mapping endpoint behavior to network evidence

---

### 🧠 SIEM Foundations & Identity Telemetry (Splunk)
📁 `SOC-SIEM-Learning/SIEM_Setup/`

This section demonstrates **how SOC telemetry is built correctly**, not just collected.

#### Labs included

**1️⃣ SOC SIEM Lab Setup**
- Phase-based VM design
- RAM-optimized execution (8 GB & 16 GB modes)
- Correct install order (Linux → Windows → AD)

**2️⃣ Splunk Enterprise + Linux Logs**
- Splunk Enterprise on Ubuntu (CLI only)
- Agentless ingestion of Linux auth & system logs
- Data validation before use

Indexes:
- `linux`

**3️⃣ Windows 10 Endpoint Telemetry**
- Advanced Audit Policy (correctly configured)
- Authentication, privilege, and process visibility
- Splunk Universal Forwarder validation

Indexes:
- `windows`

**4️⃣ Active Directory Identity Telemetry**
- Minimal AD deployment
- Credential validation & identity decisions
- Proper isolation of DC telemetry

Indexes:
- `ad`

Critical principle:
> No forwarder on the Domain Controller = no AD investigation.

---

## 🚦 How to Use This Repository

Follow this order:
1. Networking fundamentals  
2. Network traffic analysis  
3. Endpoint logging  
4. SIEM foundations (Linux → Windows → AD)

Skipping steps = broken understanding.

---

## 🧠 SOC Analyst Mindset

Instead of asking:
> “Which tool detected this?”

I focus on:
- Why this behavior exists
- Whether it is normal for this system
- How attackers abuse legitimate services
- What visibility exists (and what doesn’t)
- How SOCs detect — or miss — this activity

---

## 📌 Purpose of This Repository

Most resumes list tools.

This repository demonstrates:
- **How I investigate**
- **How I correlate evidence**
- **How I reason about traffic**
- **How I distinguish signal from noise**
- **How detection logic is built from behavior**

---

## 📈 Progress Model

Labs are added **incrementally**, grouped by skill domain:
- Networking fundamentals
- Traffic analysis
- Endpoint telemetry
- SIEM foundations
- Identity-centric investigation
- Detection logic (future)

Each lab is:
- Complete
- Documented
- Reproducible
- Interview-defensible

---

## ⚠️ Legal & Ethical Notice

All activities are conducted:
- In isolated lab environments
- On self-owned virtual machines
- For educational and defensive purposes only

No production systems or external targets are involved.
