# Graduation Vault Foundation  
## Institutional Whitepaper

**Version:** 2025  
**Status:** Canonical Reference  
**Scope:** Architecture, Governance, and Enforcement  
**Classification:** Non-Custodial Infrastructure Standard  

---

## Abstract

The Graduation Vault Foundation defines an institutional-grade, non-custodial governance framework for student-specific donation vaults.

The system uses SAFE smart accounts and Zodiac governance modules to enforce transparent, time-locked, multi-party control over donated funds — ensuring that donor intent is preserved, students are protected, and no single actor can misuse assets.

Graduation Vaults are not financial products, investment vehicles, or discretionary accounts. They are governed digital infrastructure designed to support students through graduation and transition into responsible digital ownership.

---

## 1. Problem Statement

Educational donations are traditionally managed through centralized accounts, institutional discretion, and opaque reporting.

This creates persistent risks:
- Donor intent can be diluted or overridden
- Funds may be pooled or reallocated
- Students lack transparency and agency
- Institutions bear custodial and reputational risk

Graduation Vaults address these issues by replacing trust-based controls with **cryptographically enforced governance**.

---

## 2. Design Goals

Graduation Vaults are designed to:

- Eliminate unilateral control
- Preserve donor intent
- Protect students until graduation
- Provide full transparency
- Avoid custody and investment risk
- Remain institution-compatible

The system is intentionally conservative and avoids yield, trading, or asset management features.

---

## 3. Non-Custodial Architecture

Graduation Vaults are **non-custodial by design**.

- No operator, advisor, or institution holds private keys
- No single signer can access funds alone
- All authority is shared and enforced on-chain

Infrastructure providers configure the system but never control assets.

---

## 4. System Architecture

Graduation Vaults use a layered architecture:

### 4.1 Control Layer — SAFE

SAFE smart accounts:
- Hold vault assets
- Enforce signer thresholds
- Execute transactions only after approval

SAFE is the sole execution authority.

---

### 4.2 Policy Layer — Zodiac

Zodiac modules enforce governance constraints:

- **Roles Modifier**
  - Defines proposer vs approver permissions
- **Transaction Guard**
  - Blocks unauthorized transfers
  - Enforces graduation locks
  - Prevents governance tampering

Optional timelocks may enforce graduation dates.

---

### 4.3 Presentation Layer — External Interfaces

Includes:
- Read-only dashboards
- Donor and signer visibility tools
- Educational materials

Presentation layers:
- Hold no keys
- Execute no transactions
- Possess no authority

---

## 5. Governance Model

Each Graduation Vault includes **four signers**:

1. Parent or Legal Guardian (mandatory)
2. School Representative
3. Teacher / Counselor / Staff
4. Independent Trustee or Community Oversight Member

### Thresholds
- Graduation withdrawals: **3-of-4**, Parent required
- Emergency withdrawals: **4-of-4**

This structure eliminates unilateral access.

---

## 6. Vault Lifecycle

Each vault follows a fixed lifecycle:

1. **CREATED** — Safe deployed, signers assigned
2. **ACTIVE** — Donations allowed
3. **LOCKED** — Governance changes blocked
4. **GRADUATION ELIGIBLE** — Withdrawal proposals allowed
5. **TRANSFERRED** — Funds move to Student + Parent joint SAFE

Lifecycle enforcement is on-chain and non-bypassable.

---

## 7. Graduation Payout Design

At graduation, funds are transferred to a **Student + Parent joint SAFE**.

This design:
- Prevents abrupt loss of oversight
- Introduces students to shared custody
- Allows gradual transition to full control

EOAs are explicitly prohibited as graduation destinations.

---

## 8. Emergency & Hardship Access

Emergency withdrawals are allowed only when:
- A documented hardship policy exists
- **All four signers approve**
- Withdrawals are limited to the minimum necessary amount

This preserves compassion without weakening safeguards.

---

## 9. Transparency & Auditability

Graduation Vaults are built on public infrastructure:

- All balances are visible on-chain
- All transactions are permanently recorded
- Anyone can independently verify activity

The ledger is the authoritative record.

---

## 10. What Graduation Vaults Are Not

Graduation Vaults are not:
- Bank accounts
- Investment products
- Yield-generating systems
- Discretionary scholarship funds

They do not promise returns, performance, or outcomes.

---

## 11. Change Control

Graduation Vaults are governed infrastructure.

All changes to architecture, governance, or enforcement are subject to formal change control as defined in:

`governance/change-control.md`

The on-chain SAFE configuration remains the ultimate source of truth.

---

## 12. Conclusion

Graduation Vaults replace discretionary control with enforced governance.

By combining SAFE smart accounts with Zodiac policy enforcement, the system ensures that:

- Donors can verify outcomes
- Students are protected until graduation
- Institutions reduce custodial risk
- Operators cannot interfere
- Rules are enforced by code

Graduation Vaults represent a durable, transparent model for student-centered donation infrastructure.

---

**End of Whitepaper**
