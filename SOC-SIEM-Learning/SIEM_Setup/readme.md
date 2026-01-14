# 🧠 SOC Fundamentals Labs — SIEM & Telemetry From Scratch

This repository contains **hands-on SOC lab documentation** focused on **SIEM fundamentals, log generation, log ingestion, and identity-centric investigation** using **Splunk Enterprise**.

The labs are intentionally **phase-based**, **resource-aware**, and **signal-focused**, designed to teach **how SOC data is produced, trusted, and investigated** — not just how tools are installed.

---

## 🎯 Core Philosophy

> **Splunk can only ingest what the operating system actually generates.**  
> If log generation is wrong, detection is impossible.

This repo prioritizes:
- Correct **log generation**
- Clean **data ingestion**
- Logical **index separation**
- Analyst-grade **validation**
- Minimal noise before skill

No shortcuts. No “click-next” labs.

---

## 🧩 Lab Architecture (High Level)

Linux / Windows / AD
↓
Log Generation (Audit Policy, OS behavior)
↓
Splunk Universal Forwarder (where required)
↓
Splunk Enterprise (Ubuntu Server)
↓
Indexes (linux / windows / ad)
↓
SOC Investigation & Validation


---

## 📁 Repository Structure

soc-fundamentals-labs/
│
├── SOC-SIEM-Learning/
│ ├── Foundations/
│ ├── SIEM_Setup/
│ │ ├── SOC SIEM LAB-SETUP.docx
│ │ ├── SPLUNK ENTERPRISE SETUP AND LINUX LOG INGESTION.docx
│ │ ├── SPLUNK FORWARDER SETUP & WINDOWS 10 ENDPOINT LOG INGESTION.docx
│ │ └── SPLUNK FORWARDER SETUP & WINDOWS SERVER 2019 (AD).docx
│
├── endpoint-logging-labs/
├── network-traffic-analysis/
├── networking/
└── README.md


---

## 🧪 Labs Included (Execution Order Matters)

### 1️⃣ SOC SIEM Lab Setup (Foundation)
📄 **`SOC SIEM LAB-SETUP.docx`**

Purpose:
- Host preparation
- VM planning
- Phase-based install order
- RAM-optimized design (8 GB & 16 GB modes)

Key takeaway:
> Do **not** run everything at once.  
> SOC labs break due to resource abuse, not skill gaps.

---

### 2️⃣ Splunk Enterprise + Linux Log Ingestion
📄 **`SPLUNK ENTERPRISE SETUP AND LINUX LOG INGESTION.docx`**

Purpose:
- Install Splunk Enterprise on **Ubuntu Server (CLI-only)**
- Validate Splunk health
- Ingest **Linux auth & system logs agentlessly**
- Establish trusted baseline telemetry

Indexes:
- `linux`

Key skills:
- SIEM validation
- Agentless ingestion
- Timestamp trust
- Evidence-based verification

---

### 3️⃣ Windows 10 Endpoint Log Ingestion (No AD)
📄 **`SPLUNK FORWARDER SETUP & WINDOWS 10 ENDPOINT LOG INGESTION.docx`**

Purpose:
- Configure **Advanced Audit Policy** correctly
- Generate authentication & execution telemetry
- Install and validate **Splunk Universal Forwarder**
- Ingest **Windows Security logs only**

Indexes:
- `windows`

Intentionally excluded:
- Sysmon
- PowerShell logging
- Script block logging
- Registry auditing

Why:
> Noise before skill destroys learning.

---

### 4️⃣ Active Directory Identity Telemetry
📄 **`SPLUNK FORWARDER SETUP & WINDOWS SERVER 2019 (AD).docx`**

Purpose:
- Install minimal Active Directory
- Configure **Domain Controller auditing**
- Capture **credential validation, identity decisions, and privilege escalation**
- Separate endpoint vs AD data correctly

Indexes:
- `ad`

Critical principle:
> No forwarder on the Domain Controller = no AD investigation.

---

## 🔍 What This Repo Is NOT

❌ Not a detection rule pack  
❌ Not a dashboard showcase  
❌ Not a Splunk certification dump  
❌ Not a “turn everything on” guide  

Those come **after** fundamentals.

---

## ✅ What You Learn (Practically)

- How logs are **generated**, not just collected
- Why audit policy matters more than SIEM UI
- How SOCs separate **endpoint vs identity telemetry**
- How to validate data **before trusting alerts**
- How broken time, parsing, or policy ruins investigations

---

## 🧠 Skill Level Target

- Beginner → Intermediate SOC
- Blue Team fundamentals
- SIEM foundations
- Identity-centric detection mindset

---

## 🚦 How to Use This Repo

1. Read **SOC SIEM LAB-SETUP** first  
2. Build **Linux + Splunk** before touching Windows  
3. Do **Windows 10 endpoint** before AD  
4. Add **Active Directory last**
5. Validate **every phase before moving on**

Skipping steps = broken lab.

---

## 📌 Final Note

This repository reflects **how real SOC data pipelines are built**, not how demo labs are marketed.

If you can explain *why* each step exists,  
you’re learning correctly.

---

🛡️ **Built for learning, not pretending.**
