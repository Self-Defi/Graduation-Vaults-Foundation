# Roles & Guard Manifest v1

**Graduation Vault Foundation — Governance Enforcement Specification**

---

## Purpose

This manifest defines the canonical proposer / approver / executor rules and hard enforcement constraints for Graduation Vaults using SAFE and Zodiac.

This document is authoritative for governance behavior.

---

## Signer Roles (4 Total)

- **PARENT** — Parent or Legal Guardian (mandatory signer)
- **SCHOOL** — School Representative
- **STAFF** — Teacher / Counselor / Staff
- **TRUSTEE** — Independent Trustee / Community Oversight

---

## Vault State Machine

CREATED → ACTIVE → LOCKED → GRADUATION_ELIGIBLE → TRANSFERRED

State transitions must be enforced via Guards and role restrictions.

---

## Action Classes

Policies apply across four action classes:
1. Inbound Donations (permissionless)
2. Graduation Withdrawals
3. Emergency / Hardship Withdrawals
4. Configuration Changes

---

## Graduation Withdrawals (Standard Path)

### Proposers
- PARENT
- SCHOOL
- STAFF
- TRUSTEE

### Approvers
- All four may approve

### Threshold
- 3-of-4 required
- Parent signature mandatory

### Destination Constraint
Graduation withdrawals may only execute to:
- A **Student + Parent joint SAFE** created for graduation handoff

EOA destinations are prohibited.

### Timing Constraint
Graduation withdrawals are blocked until the vault is in:
- GRADUATION_ELIGIBLE

### Executor
- PARENT or TRUSTEE

---

## Emergency / Hardship Withdrawals (Exception Path)

### Proposers
- PARENT
- TRUSTEE

### Approvers
- 4-of-4 required (full consensus)

### Constraints
- Withdrawal amount must be explicitly specified
- Withdrawals must be minimal
- Destination must be an approved hardship destination

### Executor
- PARENT or TRUSTEE

---

## Configuration Changes

Includes:
- Adding/removing signers
- Changing thresholds
- Adding/removing modules
- Adding/removing/modifying guards

### Proposers
- TRUSTEE

### Approvers
- 4-of-4 required

### State Constraints
- CREATED: allowed
- ACTIVE: allowed (restricted)
- LOCKED: blocked
- GRADUATION_ELIGIBLE: blocked
- TRANSFERRED: blocked

Signer replacement in ACTIVE is allowed only for key loss or role turnover, and must retain the four-role model.

---

## LOCKED State Enforcement

When the vault is LOCKED:
- No signer changes
- No threshold changes
- No module changes
- No guard changes
- No outbound transfers

Exception:
- Emergency / hardship withdrawals (4-of-4 only)

---

## Guard-Level Hard Rules

Guards must block:
- Any outbound transfer without Parent approval
- Any outbound transfer before GRADUATION_ELIGIBLE
- Transfers to non-approved destinations (including EOAs)
- Any configuration change in LOCKED or later states
- Any signer removal that would eliminate Parent role

Guards override role permissions if rules are violated.

---

## Non-Custodial Assertion

This manifest grants no authority to operators, advisors, or implementation partners.

They have:
- No signing authority
- No proposal authority
- No execution authority

All authority remains with the defined signer roles.

---

## Status

- Version: v1.0
- Status: Production-ready baseline
- Change Control: Required
- Enforcement: On-chain

