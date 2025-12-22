# Network Traffic Analysis — SOC Labs

This folder contains hands-on **SOC-focused network traffic analysis labs** designed to build strong fundamentals in identifying **normal vs suspicious network behavior** across DNS, HTTP, and Firewall telemetry.

The emphasis is on **behavioral analysis, traffic flow, and context**, not tools, exploits, or signatures.

These labs are built to train **how SOC analysts think**, not just how they run commands.

---

## 📁 Labs Included

---

## 1️⃣ DNS Labs (`DNS-labs.docx`)

Focuses on DNS query and response behavior, including how attackers abuse DNS during early stages of compromise.

### Key concepts covered
- Normal DNS resolution flow
- NXDOMAIN responses and their significance
- High-frequency DNS queries
- Random / high-entropy domains (DGA simulation)
- TXT record awareness

### SOC skills gained
- Detecting early-stage malware activity
- Identifying DNS-based beaconing and DGA behavior
- Understanding why DNS is often the **first signal of compromise**

---

## 2️⃣ HTTP Labs (`http-labs.docx`)

Focuses on HTTP traffic patterns and how attackers blend malicious activity into normal-looking web traffic.

### Key concepts covered
- HTTP GET vs POST behavior
- User-Agent analysis
- Suspicious URI patterns
- HTTP status code interpretation
- Repetitive HTTP requests (beaconing simulation)
- Content-Type awareness

### SOC skills gained
- Distinguishing human vs automated traffic
- Detecting HTTP-based C2 communication
- Identifying phishing, tracking, and malware delivery indicators

---

## 3️⃣ Firewall, Endpoint & Attacker Correlation Lab  
📂 `firewall-endpoint-attacker-correlation/`

This lab focuses on **firewall visibility, traffic direction, and multi-system correlation** using a realistic SOC-style setup.

It connects **attacker behavior, firewall logs, and endpoint context** into a single investigation workflow.

### Lab architecture

Kali Linux (Attacker)
|
v
Ubuntu Server (Firewall + Logs)
|
v
Windows 11 (Endpoint / Client)


### Key concepts covered
- Inbound vs outbound traffic analysis
- UFW ALLOW vs BLOCK interpretation
- SRC / DST / SPT / DPT field analysis
- Port scanning detection patterns
- Allowed outbound traffic risk (C2-style behavior)
- Firewall visibility boundaries

### Scenarios simulated
- Kali → Ubuntu port scan (blocked inbound attack)
- Windows → Ubuntu SSH (legitimate internal access)
- Ubuntu → Internet HTTP traffic (allowed outbound risk)
- Windows → Internet traffic bypassing firewall
- Correlation across attacker, firewall, and endpoint

### SOC skills gained
- Differentiating attack traffic from normal business activity
- Understanding why **allowed traffic is not always safe**
- Knowing when firewall logs are sufficient — and when they are not
- Thinking in terms of **attacker, victim, and endpoint roles**
- Explaining traffic behavior clearly in SOC interviews

---

## 🧪 Lab Environment

- **Kali Linux** — attacker and traffic generation
- **Ubuntu Server** — firewall, logging, and control point
- **Windows 11** — endpoint / user activity

### Tools used
- `nmap`
- `curl`
- `ping`
- Native firewall logging (UFW)

No SIEM, IDS, proxy, or EDR tools are used at this stage to keep the focus on **network fundamentals and analyst reasoning**.

---

## 🎯 SOC Perspective

These labs are intentionally:

- Tool-agnostic  
- Detection-focused  
- Correlation-driven  
- Interview-defensible  

Each lab emphasizes:
- **Patterns over single events**
- **Behavior over reputation**
- **Context over alerts**
- **Visibility boundaries over assumptions**

---

## 📌 Note

These labs are part of a broader **SOC fundamentals learning path** and are continuously expanded as new traffic patterns, attack techniques, and correlation scenarios are added.

The goal is to build **strong SOC intuition**, not just checklist knowledge.
