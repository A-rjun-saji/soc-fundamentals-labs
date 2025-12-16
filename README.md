# 🛡️ SOC Fundamentals Labs

> Hands-on SOC labs focused on **attacker behavior**, **detection mindset**, and **real analyst workflows**.  
> Built to prove practical SOC skills — not tool memorization.

---

## 🔍 What This Repository Proves

✔ Core **SOC L1 fundamentals**  
✔ Understanding of **network & system behavior**  
✔ Ability to **translate activity into detections**  
✔ Analyst thinking beyond alerts and dashboards  

This is **not a tutorial repository**.  
This is **evidence of hands-on SOC capability**.

---

## 🧪 Lab Environment

| Component | Role |
|---------|-----|
| Kali Linux | Attacker / probing |
| Windows 10 | Enterprise endpoint |
| Windows 7 | Legacy / high-risk endpoint |
| Windows 11 + WSL | Linux services / pseudo-C2 |
| Network | Host-only / NAT (isolated) |

---

## 📂 Lab Categories

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

## 🧠 SOC Analyst Mindset

Instead of asking:
> “Which tool is this?”

I focus on:
- Why this behavior is suspicious
- How attackers abuse normal services
- What this looks like in logs
- How a SOC would detect or miss it

---

## 📌 Purpose of This Repository

Most resumes list tools.

This repository shows:
- **How I think**
- **What I investigate**
- **Why behavior matters**
- **How activity maps to detection**

---

## 📈 Progress Model

Labs are added **incrementally**, grouped by skill domain:
- Networking
- DNS & HTTP
- Windows & Linux logs
- Detection logic
- SIEM correlation (future)

Each lab is **complete, documented, and reproducible**.

---

## ⚠️ Legal & Ethical Notice

All activities are conducted:
- In isolated lab environments
- On self-owned virtual machines
- For educational and defensive purposes only

No production systems are involved.

---


