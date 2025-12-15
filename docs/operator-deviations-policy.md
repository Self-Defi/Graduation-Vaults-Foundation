# Operator Deviations & Extensions Policy

**Graduation Vault Foundation — Ecosystem Governance Standard**

---

## Purpose

This policy defines what operators may change, what operators must never change, and how deviations are formally approved across the Graduation Vault ecosystem.

It exists to:
- Prevent governance drift across schools and cohorts
- Protect students, donors, and institutions
- Protect operators from being pressured into unsafe changes
- Preserve Graduation Vaults as institution-grade, non-custodial infrastructure

---

## Operator Definition

An Operator is any person or entity responsible for configuring, deploying, or maintaining Graduation Vault infrastructure **without custody or governance authority**.

Operators:
- Configure SAFE + Zodiac according to approved templates
- Do not hold keys
- Do not approve transactions
- Do not execute withdrawals
- Do not override governance rules

---

## Non-Negotiable Invariants (Must Not Change)

No deviation is permitted under any circumstance.

1. **Non-Custodial Architecture**
   - Operators must never hold private keys
   - Operators must never be added as signers

2. **Donation-Only Designation**
   - No yield strategies
   - No investment representations
   - No pooling of student funds
   - No discretionary asset management

3. **Mandatory Parent / Guardian Role**
   - Parent/Guardian remains a mandatory signer
   - Role cannot be removed, bypassed, or replaced

4. **Graduation Lock Enforcement**
   - Funds locked until graduation eligibility
   - Early withdrawals only via documented hardship path

5. **Governance Threshold Floors**
   - Graduation withdrawals: minimum 3-of-4
   - Emergency withdrawals: 4-of-4 only

6. **Destination Safety**
   - Graduation payouts go only to Student + Parent joint SAFE
   - EOAs are prohibited as graduation destinations

---

## Operator-Level Configurations (May Change)

Operators may adjust the following without additional approval:

- Network selection (SAFE + Zodiac supported)
- Graduation date / timelock parameters per student
- Signer identity within roles (School/Staff/Trustee) due to staffing changes
- Presentation layer branding and dashboards (read-only)

Operators may not change role count, thresholds, or enforcement logic.

---

## Conditional Deviations (Require Formal Approval)

The following changes require documented signer approval and recordkeeping:

- Increasing thresholds above baseline
- Adding additional guards that increase restrictions
- Extending lock durations beyond baseline
- Hardship policy customization (without reducing approvals)

Decreasing thresholds, weakening restrictions, or bypassing locks is prohibited.

---

## Prohibited Changes (Never Allowed)

The following actions invalidate the Graduation Vault deployment:

- Adding operators as signers
- Allowing EOAs as graduation payout destinations
- Removing Transaction Guards or Roles Modifiers
- Enabling yield, staking, strategy execution, or asset management
- Allowing withdrawals without Parent approval
- Modifying governance in LOCKED state without formal approval

---

## Deviation Approval Process

When an allowed deviation is requested:

1. Document the requested change
2. Provide rationale
3. Provide impact assessment
4. Obtain signer approval (per Change Control requirements)
5. Record the decision and effective date
6. Record Safe address(es) affected

Unrecorded deviations are not permitted.

---

## Enforcement

This policy is enforced via:
- SAFE thresholds
- Zodiac Roles and Guards
- Formal Change Control

Failure to adhere is a governance breach.

---

## Status

- Version: v1.0
- Scope: Ecosystem baseline
- Change Control: Required

---

**Graduation Vaults are infrastructure — not discretion.**

