# Roles & Guard Manifest v1

**Graduation Vault Foundation — Governance Enforcement Specification**

---

## Purpose

This manifest defines **proposer, approver, executor rules** and **hard enforcement constraints** for Graduation Vaults using SAFE and Zodiac.

This document is authoritative for governance behavior.

---

## Signer Roles

- PARENT — Mandatory signer
- SCHOOL — Operational governance
- STAFF — Student-centered oversight
- TRUSTEE — Independent oversight

---

## Vault States

CREATED → ACTIVE → LOCKED → GRADUATION_ELIGIBLE → TRANSFERRED

State transitions are enforced by Guards and role restrictions.

---

## Graduation Withdrawal Rules

**Proposers:** All signers  
**Approvers:** 3-of-4 required  
**Mandatory:** Parent signature  
**Destination:** Student + Parent joint SAFE  
**Executor:** Parent or Trustee  

Withdrawals before graduation eligibility are blocked.

---

## Emergency / Hardship Rules

**Proposers:** Parent or Trustee  
**Approvers:** 4-of-4 required  
**Executor:** Parent or Trustee  

Withdrawals must be minimal and documented.

---

## Configuration Change Rules

**Proposers:** Trustee  
**Approvers:** 4-of-4 required  

Blocked entirely in LOCKED and later states.

---

## Guard-Level Enforcement

Guards must block:
- Outbound transfers without Parent approval
- Transfers before graduation eligibility
- EOAs as destinations
- Governance changes in LOCKED state
- Removal of Parent role

Guards override role permissions.

---

## Non-Custodial Assertion

No operator, advisor, or platform has:
- Signing authority
- Proposal authority
- Execution authority

---

## Status

- Version: v1.0
- Enforcement: On-chain
- Change Control: Required
