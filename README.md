# Graduation-Vaults-Foundation  
## GV-Foundation

**Institutional-grade, non-custodial governance standards for Graduation Vaults**

---

## Purpose

GV-Foundation defines the **canonical architecture, governance rules, and operational boundaries** for Graduation Vaults.

This repository is **not** a product, protocol, or platform.  
It is a **governed reference standard** used to deploy, operate, and audit student-specific donation vaults built on **SAFE smart accounts** and **Zodiac governance modules**.

All documents in this repository describe **enforced behavior**, not discretionary policy.

---

## What Graduation Vaults Are

Graduation Vaults are **student-specific donation vaults** designed to:

- Protect donor intent
- Prevent unilateral control
- Lock funds until graduation or documented hardship
- Provide full transparency and auditability
- Eliminate custodial and discretionary risk

They are intentionally conservative and **do not** include yield, investment, or asset management features.

---

## Repository Structure

This repository is organized as a **standards library**, not an application codebase.

/
├─ README.md
├─ docs/
│ ├─ index.md
│ ├─ architecture-overview.md
│ ├─ gv-whitepaper.md
│ ├─ operator-quickstart.md
│ ├─ operator-deviations-policy.md
│ ├─ signer-onboarding.md
│ ├─ donor-transparency.md
│ └─ rules-guard-manifest.md
├─ governance/
│ └─ change-control.md
└─ assets/
└─ pdfs/
└─ gv-whitepaper-2025.pdf


---

## Documentation Index (Start Here)

📘 **Canonical Documentation Index**  
→ **/docs/index.md**

This index routes readers to the correct documents based on their role.

---

## Core Foundation

These documents define **what the system is** and **what cannot change**.

- **Whitepaper (PDF)**  
  Institutional-grade design rationale, lifecycle, and compliance framing  
  → https://raw.githubusercontent.com/Self-Defi/Graduation-Vaults-Foundation/main/assets/pdfs/gv-whitepaper-2025.pdf

- **Whitepaper (Markdown)**  
  Canonical GitHub-readable version  
  → /docs/gv-whitepaper.md

- **Architecture Overview**  
  Control, policy, and presentation layer separation  
  → /docs/architecture-overview.md

---

## Governance & Enforcement

These documents define **how authority works** and **what is enforced**.

- **Roles & Guard Manifest v1**  
  Proposer / approver / executor rules and hard enforcement constraints  
  → /docs/rules-guard-manifest.md

- **Change Control Policy**  
  Authoritative governance for all modifications  
  → /governance/change-control.md

---

## Operations

These documents define **how the system is deployed correctly**.

- **Operator Quickstart**  
  Base SAFE + Zodiac deployment template  
  → /docs/operator-quickstart.md

- **Operator Deviations & Extensions Policy**  
  What operators may change, what must never change  
  → /docs/operator-deviations-policy.md

---

## Human-Facing Governance

These documents are written for **non-technical stakeholders**.

- **Signer Onboarding & Responsibilities**  
  Plain-language guide for parents, staff, and trustees  
  → /docs/signer-onboarding.md

- **Donor Transparency & Expectations**  
  Plain-language guide for donors and sponsors  
  → /docs/donor-transparency.md

---

## Non-Custodial Assertion

At no point does GV-Foundation grant any operator, advisor, or implementation partner:

- Signing authority
- Proposal authority
- Execution authority
- Fund management responsibility

All authority remains with the defined signer roles and is enforced on-chain.

---

## Document Authority

- On-chain SAFE configuration is the **ultimate source of truth**
- Documentation exists to **describe**, not override, enforcement
- Governance changes require explicit approval and recordkeeping

**GV-Foundation does not drift.**

---

## Status

**Canonical Reference Standard**  
Applies to all Graduation Vault deployments using GV-Foundation
