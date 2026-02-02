# Elastic Security EDR — End-to-End Lab Build

This folder contains a **complete, enterprise-style Elastic Security (EDR + SIEM) lab build guide**.

The focus of this lab is **not installation success**, but **operational correctness**:
verifying raw endpoint telemetry, understanding Fleet-managed control flow, and avoiding false confidence from UI-only checks.

---

## 🎯 Lab Objective

Build and validate a **fully functional Elastic EDR pipeline**, including:

- Elastic Stack control plane (Elasticsearch, Kibana, Fleet Server)
- Fleet-managed Elastic Agent
- Windows endpoint with high-fidelity telemetry
- Deterministic validation gates using raw data

This lab treats **Discover as ground truth**, not dashboards or agent status.

---

## 🧱 Architecture Overview

**Control Plane (Ubuntu Server):**
- Elasticsearch (data store + TLS authority)
- Kibana (Security UI, detections, Fleet)
- Fleet Server (agent control plane)

**Endpoint (Windows 10):**
- Sysmon (process, file, network telemetry)
- Elastic Agent with Elastic Defend integration

**Control Flow:**

Endpoint (Elastic Agent)
↓
Fleet Server
↓
Kibana (policies & outputs)
↓
Elasticsearch (raw events)


> Critical rule: **Agents blindly follow Fleet.  
If Fleet or Kibana is misconfigured, EDR silently fails.**

---

## 📘 What This Lab Teaches (Beyond Setup)

- Why “Agent = Healthy” does **not** mean “EDR = Working”
- How backend misconfiguration breaks every endpoint
- Why version mismatches silently kill telemetry
- How TLS paths and permissions affect Fleet outputs
- How SOC teams validate detections **from raw events upward**

---

## ✅ Success Criteria (Hard Gates)

This lab is considered **successful only if**:

- `agent.type : "endpoint"` returns data in Discover
- Process events are visible (`endpoint.events.process`)
- File events are visible (`endpoint.events.file`)
- Network events are visible (`endpoint.events.network`)
- Events are **continuous and recent**

If these are missing, the lab is intentionally considered **failed**.

---

## 📂 Contents

- **Elastic-Security-EDR-Lab-Build-Guide.docx**
  - Line-by-line lab build guide
  - Backend-first validation approach
  - Common failure modes and real fixes
  - Enterprise-aligned EDR mindset

> PDF version is recommended for final review and sharing.

---

## 👤 Intended Audience

- SOC beginners
- Blue team learners
- Security analysts preparing for SOC roles
- Anyone wanting **real EDR understanding**, not demo success

This assumes:
- Basic Linux and Windows familiarity
- Willingness to stop and fix failures instead of skipping ahead

---

## ⚠️ What This Is NOT

- Not a YouTube-style “it should work” lab
- Not a copy-paste deployment guide
- Not focused on alerts or dashboards first

This is an **EDR fundamentals lab**, grounded in telemetry.

---

## 🧠 Why This Matters

Enterprise SOCs trust **data**, not UI indicators.

This lab trains the same mindset:
- Validate first
- Detect second
- Respond last

If you understand this lab, you understand **how EDR actually works**.
