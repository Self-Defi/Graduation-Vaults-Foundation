# Graduation Vault Foundation — Architecture Overview

---

## Architectural Objective

The Graduation Vault Foundation defines a **governed, non-custodial architecture** for student-specific donation vaults.

The system prioritizes:
- Protection of donor intent
- Student-first governance
- Institutional transparency
- Elimination of discretionary control

---

## Layered Architecture Model

Graduation Vaults are implemented using **three strictly separated layers**.

---

## 1. Control Layer — SAFE

**Role:** Asset custody and execution

SAFE smart accounts:
- Hold vault assets
- Enforce signer thresholds
- Execute transactions only after governance approval

Key properties:
- No single signer control
- No operator access
- No discretionary execution

SAFE is the **only entity capable of moving funds**, and only under approved conditions.

---

## 2. Policy Layer — Zodiac

**Role:** Governance enforcement and restriction

Implemented using Zodiac modules:

- **Roles Modifier**
  - Defines proposer vs approver permissions
  - Restricts execution authority

- **Transaction Guard**
  - Blocks unauthorized transfers
  - Enforces graduation locks
  - Prevents governance tampering

Optional:
- Timelock or graduation trigger

Zodiac ensures that **even valid signatures cannot bypass policy**.

---

## 3. Presentation Layer — External Interfaces

**Role:** Transparency and education

Includes:
- Read-only dashboards
- Donor and signer visibility tools
- Educational materials
- Transaction construction assistance

Constraints:
- No private keys
- No transaction execution
- No governance authority

Presentation layers are **informational only**.

---

## Graduation Vault Lifecycle Enforcement

Each vault follows a fixed lifecycle:

1. CREATED
2. ACTIVE
3. LOCKED
4. GRADUATION ELIGIBLE
5. TRANSFERRED

Lifecycle transitions are enforced via:
- Zodiac Guards
- Role restrictions
- Optional timelock logic

Manual overrides are not permitted.

---

## Governance Model Summary

- 4 signers per vault
- Parent / Guardian is mandatory
- Graduation withdrawals: 3-of-4 (Parent required)
- Emergency withdrawals: 4-of-4
- Graduation payout → Student + Parent joint SAFE

This model eliminates unilateral control.

---

## Trust Boundaries

| Actor | Authority |
|---|---|
| Student | View-only (pre-graduation) |
| Parent / Guardian | Mandatory signer |
| School | Governance participant |
| Trustee | Independent oversight |
| Operator | Configuration only |
| SD Advisory | Infrastructure & education only |

No actor crosses trust boundaries.

---

## Design Outcome

This architecture ensures:
- Donor funds cannot be misused
- Students are protected until graduation
- Operators cannot interfere
- Governance is cryptographically enforced

Graduation Vaults function as **governed infrastructure**, not accounts or products.

---

## Status

- Architecture: Locked
- Enforcement: On-chain
- Auditability: Continuous

