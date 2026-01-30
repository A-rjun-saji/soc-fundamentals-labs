# EDR Prerequisites

This folder contains **mandatory foundational knowledge** required before working with any Endpoint Detection & Response (EDR) tools or labs.

This is not optional reading.

---

## Why This Exists

EDR is **not** a malware scanner.  
It is a **high-fidelity telemetry and behavior correlation system**.

Without a solid understanding of:
- how Windows endpoints actually work,
- how processes execute and use memory,
- how identity, credentials, and persistence function,
- and how analysts should reason about alerts,

EDR alerts become **noise**, and tooling amplifies mistakes instead of skill.

This folder exists to enforce that baseline.

---

## What You Must Understand Before Proceeding

Before starting any EDR labs, you are expected to be comfortable reasoning about:

- Endpoint internals (processes, threads, services, registry, file system)
- Execution flow and memory behavior
- Fileless execution and trusted binary abuse
- Identity, credentials, and LSASS risk
- Persistence mechanisms
- Telemetry, logging, and correlation thinking
- Analyst discipline and response impact

If these concepts are unclear, **do not proceed to labs**.

---

## Contents

- **`edr-prerequisites-core-knowledge.pdf`**  
  Complete baseline knowledge required for effective EDR analysis.

---

## Scope Boundary

This folder is **intentionally static**.

- No labs
- No tools
- No vendor content
- No screenshots

It serves as a **gate** to ensure readiness.

Core and vendor-specific labs will be introduced later in:
- `edr-core-labs`
- `edr-vendor-labs`

Only after these prerequisites are understood.

---

## Analyst Expectation

EDR does not make decisions.  
**Analysts do.**

This document defines the minimum thinking standard expected before touching an EDR console.
