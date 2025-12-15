# Operator Quickstart

**Graduation Vault Foundation — Base Deployment Template**

---

## Operator Scope

Operators configure SAFE + Zodiac according to this template.

Operators do **not**:
- Hold private keys
- Approve transactions
- Execute withdrawals
- Deviate from this template without signer approval

---

## Preconditions

Before deployment:
- Correct network selected
- Four signer addresses verified
- Graduation year documented
- Graduation destination = Student + Parent joint SAFE

---

## Step 1 — Create the Vault SAFE

- Name: `GV — <Student> — <Grad Year>`
- Signers: 4
- Threshold: 3-of-4

---

## Step 2 — Install Zodiac Modules

Required:
- Roles Modifier
- Transaction Guard

Optional:
- Timelock (graduation trigger)

---

## Step 3 — Apply Governance Rules

- All signers may propose
- Parent signature required for withdrawals
- Graduation withdrawal → Student + Parent SAFE
- Emergency withdrawals → 4-of-4

---

## Step 4 — Lock Configuration

Before entering LOCKED:
- Verify signer set
- Verify guard enforcement
- Test blocked transactions

---

## Step 5 — Graduation Execution

- Create withdrawal proposal
- Collect 3 approvals (Parent required)
- Execute via Parent or Trustee

---

## Documentation Required

Record:
- Safe address
- Signer roles
- Graduation date
- Enabled guards

---

## Final Note

Operators facilitate setup only.  
Governance belongs to signers.  
Enforcement belongs to code.

---

**Status:** Canonical Operator Template
