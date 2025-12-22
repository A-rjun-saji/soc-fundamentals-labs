# 🛡️ SOC Fundamentals Labs

> Hands-on SOC labs focused on **attacker behavior**, **network & host visibility**, and **real analyst workflows**.  
> Built to prove **how I think as a SOC analyst**, not what tools I can click.

This repository is designed to demonstrate **practical SOC capability**, not certification prep or tool memorization.

---

## 🔍 What This Repository Proves

✔ Core **SOC L1 fundamentals**  
✔ Understanding of **network, firewall, and endpoint behavior**  
✔ Ability to **differentiate normal vs suspicious activity**  
✔ Skill in **correlating attacker, victim, and endpoint evidence**  
✔ Analyst thinking **beyond alerts, dashboards, and signatures**

This is **not a tutorial repository**.  
This is **evidence of hands-on SOC investigation skills**.

---

## 🧪 Lab Environment

| Component | Role |
|--------|------|
| Kali Linux | Attacker / scanning / probing |
| Ubuntu Server | Firewall, logging, control point |
| Windows 11 | Enterprise endpoint / user activity |
| Windows 10 | Secondary endpoint |
| Windows 7 | Legacy / high-risk endpoint |
| Network | Host-only / NAT (isolated lab) |

All traffic and activity is **fully controlled and observable**.

---

## 📂 Lab Categories

---

### 🌐 Networking Fundamentals  
📁 `networking/`

**Skills covered**
- TCP/IP 3-way handshake (packet-level understanding)
- Ports vs protocols (common SOC misconception)
- Trusted port abuse (443 ≠ HTTPS)
- Netcat usage (C2-style communication)

Each lab contains:
- 🎯 Objective  
- 🧱 Lab setup  
- ⚙️ Commands executed  
- 👀 Observations  
- 🧠 SOC takeaway  
- 🚨 Detection angle  

---

### 🌐 Network Traffic Analysis  
📁 `network-traffic-analysis/`

Focuses on **DNS, HTTP, and Firewall traffic** with an emphasis on **behavioral patterns and visibility boundaries**.

**Skills covered**
- DNS resolution flow and abuse patterns
- HTTP request behavior and beaconing indicators
- Firewall ALLOW vs BLOCK interpretation
- Inbound vs outbound traffic analysis
- SRC / DST / SPT / DPT field analysis
- Visibility gaps (what firewalls can and cannot see)

Includes a full **Firewall + Endpoint + Attacker correlation lab** demonstrating:
- Blocked inbound scans
- Legitimate internal access
- Risky allowed outbound traffic
- Endpoint traffic bypassing firewall visibility
- SOC-style correlation and decision-making

---

### 🖥️ Endpoint Logging & System Behavior  
📁 `endpoint-logging-labs/`

Focuses on **host-level visibility** from Windows and Linux systems.

**Skills covered**
- Windows authentication and process activity
- Linux authentication and service logs
- Differentiating system noise from attacker behavior
- Mapping endpoint activity to network evidence

---

## 🧠 SOC Analyst Mindset

Instead of asking:
> “Which tool detected this?”

I focus on:
- Why this behavior exists
- Whether it is normal for this system
- How attackers abuse normal services
- What this looks like across **firewall + endpoint + network**
- How a SOC would detect it — or miss it

---

## 📌 Purpose of This Repository

Most resumes list tools.

This repository demonstrates:
- **How I investigate**
- **How I correlate evidence**
- **How I reason about traffic**
- **How I distinguish signal from noise**
- **How behavior maps to detection logic**

---

## 📈 Progress Model

Labs are added **incrementally**, grouped by skill domain:
- Networking fundamentals
- DNS & HTTP analysis
- Firewall traffic & visibility
- Windows & Linux logging
- Detection logic & correlation
- SIEM-based detection (future)

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
