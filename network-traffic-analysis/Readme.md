# Network Traffic Analysis — SOC Labs

This folder contains hands-on **SOC-focused network traffic analysis labs**.
The labs are designed to build strong fundamentals in identifying **normal vs suspicious behavior** at the DNS and HTTP layers.

The emphasis is on **behavioral analysis**, not tools or exploitation.

---

## 📁 Labs Included

### 1️⃣ DNS Labs (`DNS-labs.docx`)
Focuses on DNS query/response behavior and common abuse patterns.

**Key concepts covered:**
- Normal DNS resolution flow
- NXDOMAIN responses and their significance
- High-frequency DNS queries
- Random / high-entropy domains (DGA simulation)
- TXT record awareness

**SOC skills gained:**
- Detecting early-stage malware activity
- Identifying DNS-based beaconing and DGA behavior
- Understanding why DNS is often the first signal of compromise

---

### 2️⃣ HTTP Labs (`http-labs.docx`)
Focuses on HTTP requests, headers, and common web-based indicators.

**Key concepts covered:**
- HTTP GET vs POST behavior
- User-Agent analysis
- Suspicious URI patterns
- HTTP status code interpretation
- Repetitive HTTP requests (beaconing simulation)
- Content-Type awareness

**SOC skills gained:**
- Distinguishing human vs automated traffic
- Detecting HTTP-based C2 communication
- Identifying phishing, tracking, and malware delivery indicators

---

## 🧪 Lab Environment

- Kali Linux (traffic generation and simulation)
- Windows (host / endpoint perspective)
- Tools: `curl`, `nslookup`

No SIEM or proxy tools are used at this stage to keep the focus on **protocol fundamentals**.

---

## 🎯 SOC Perspective

These labs are intentionally:
- Tool-agnostic
- Detection-focused
- Interview-defensible

Each lab emphasizes:
- **Patterns over single events**
- **Behavior over reputation**
- **Early indicators over post-compromise artifacts**

---


## 📌 Note

These labs are part of a larger **SOC fundamentals learning path** and are continuously expanded as more topics are added.
