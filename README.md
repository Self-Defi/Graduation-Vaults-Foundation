# Graduation Vault Foundation

**An institutional-grade, non-custodial governance framework for student donation vaults**

> **Governance Notice:**  
> This repository is governed by formal change control. All modifications are subject to the policies defined in `governance/change-control.md`.

---

## Overview

The **Graduation Vault Foundation** defines the canonical technical and governance architecture for implementing Graduation Vaults using **SAFE smart accounts** and **Zodiac modular governance**.

This repository is **not** a wallet, **not** a custody platform, and **not** an investment product.

It is a reference foundation that schools, communities, and implementation partners can adopt to deploy **donation-only, time-locked, student-specific vaults** with cryptographically enforced governance.

The design is intentionally conservative and institution-ready:

- No custody  
- No pooled funds  
- No yield strategies  
- No discretionary asset management  

All rules are enforced **on-chain**, auditable by any third party, and aligned with long-term student outcomes.

---

## Core Principles (Non-Negotiable)

### Non-Custodial by Design
SD Advisory Group and Self-Defi never hold private keys, never initiate transactions, and never have the ability to move funds.

### Donation-Only Architecture
Funds enter vaults as donations or gifts. There are no representations of return, yield, or investment performance.

### Student-Specific Vaults
Each vault corresponds to a single student and a defined graduation target.

### Governance First
All withdrawals require multi-signature approval, with a Parent or Guardian as a mandatory signer.

### Time-Locked Graduation Enforcement
Funds are cryptographically restricted until graduation conditions are met.

### Radical Transparency
All balances and transactions are publicly verifiable on-chain.

---

## System Architecture

The Graduation Vault System is composed of three distinct layers:

### 1. Control Layer (SAFE)
- SAFE smart account  
- Holds assets  
- Enforces signer thresholds  
- Executes approved transactions  

### 2. Policy Layer (Zodiac)
- Transaction Guards (what cannot happen)  
- Role Modifiers (who can propose vs approve)  
- Optional time-based or event-based automation  

### 3. Presentation Layer (External)
- Read-only dashboards  
- Education and disclosures  
- Transaction construction assistance  

**Important:** Presentation layers never hold keys and never execute transactions.

---

## Graduation Vault Lifecycle

Every Graduation Vault follows a fixed, ordered lifecycle:

1. **CREATED**  
   Safe is deployed, signers assigned, graduation target recorded.

2. **ACTIVE**  
   Donations allowed. Governance configuration is fixed.

3. **LOCKED**  
   Signer changes and policy changes are blocked.

4. **GRADUATION ELIGIBLE**  
   Graduation conditions met; withdrawal proposal may be created.

5. **TRANSFERRED**  
   Funds released to a **Student + Parent joint SAFE**.

Lifecycle transitions are enforced using Zodiac Guards and Role restrictions.

---

## Base Governance Model

### Signer Set (4)
- Parent or Guardian (**mandatory signer**)  
- School Representative  
- Teacher / Counselor  
- Independent Trustee or Community Oversight Member  

### Thresholds
- **3-of-4** for graduation withdrawals  
- **4-of-4** for emergency or hardship withdrawals  

No single party can unilaterally access funds.

---

## Zodiac Modules (Standardized)

### Required Modules
- **Roles Modifier** — defines proposer vs approver permissions  
- **Transaction Guard** — enforces donation-only and graduation locks  

### Optional (Conservative)
- Timelock or graduation trigger  

### Explicitly Excluded
- Yield automation  
- Strategy execution  
- Asset rebalancing  
- Discretionary fund management  

---

## Emergency & Hardship Access

Emergency withdrawals are allowed only when:
- A documented hardship policy exists  
- **All four signers approve**  
- Withdrawals are limited to the minimum necessary amount  

This preserves compassion without undermining long-term protection.

---

## Trust Boundaries

| Actor | Capabilities |
|---|---|
| Student | View-only access pre-graduation |
| Parent / Guardian | Mandatory signer |
| School | Governance participant |
| Trustee | Independent oversight |
| SD Advisory | Infrastructure & education only |

At no point does SD Advisory hold keys or gain transaction authority.

---

## What This Repository Is Not

- A wallet UI  
- A custody solution  
- A DeFi protocol  
- A yield product  
- A financial advisory service  

This foundation exists to **encode donor intent and student protection into infrastructure**.

---

## Change Control & Governance

GV-Foundation is treated as **governed infrastructure**, not an evolving product or informal documentation set.

All changes to architecture, governance rules, operator procedures, signer models, or enforcement logic are subject to formal change control.

### Authoritative Policy
All modifications to GV-Foundation standards are governed by:

**`governance/change-control.md`**

This includes (but is not limited to):
- Signer role definitions and thresholds  
- Graduation and emergency withdrawal rules  
- Operator permissions and limitations  
- Zodiac Roles and Guard behavior  
- Lock conditions and lifecycle enforcement  

### No Silent Changes
Governance-affecting changes must not be made informally, implicitly, or through operational shortcuts.

Such changes require:
- Explicit documentation  
- Defined rationale and impact assessment  
- Appropriate approval per the Change Control policy  
- Versioning and permanent recordkeeping  

### Source of Truth
The on-chain SAFE configuration remains the ultimate source of truth.  
Documentation exists to describe — not override — enforced behavior.

**GV-Foundation does not drift.**

---

## Related Repositories

- Graduation Vault HUB (dashboards & education)  
- SAFE Global core contracts  
- Gnosis Guild Zodiac modules  

---

## License & Disclosure

This repository provides **infrastructure patterns only**. It does not provide financial advice, investment services, or custodial functions.

Schools and organizations should consult legal counsel before integrating Graduation Vaults with existing scholarship, nonprofit, or educational programs.

---

## Status

**Production-ready reference architecture**  
Deployed using battle-tested SAFE and Zodiac infrastructure.
