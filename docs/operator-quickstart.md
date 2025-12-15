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

Before deployment, confirm:

- Network selected (SAFE + Zodiac supported)
- Four signer addresses verified
- Signer identities mapped to roles (Parent / School / Staff / Trustee)
- Graduation year recorded
- Graduation destination will be a **Student + Parent joint SAFE**
- Operator has no signer role and no signing access

---

## Step 1 — Create the Graduation Vault SAFE

In Safe:

- Name: `GV — <Student> — <Grad Year>`
- Signers: 4
- Threshold: 3-of-4

Confirm the Parent/Guardian signer is included and recorded as mandatory.

---

## Step 2 — Install Zodiac Modules

Required:
- Roles Modifier
- Transaction Guard

Optional (conservative):
- Timelock / graduation trigger

Do not install modules that introduce yield, strategy execution, or discretionary automation.

---

## Step 3 — Apply Base Governance Rules

Configure Roles + Guard enforcement to match the Foundation baseline:

### Proposals
- All signers may create proposals for graduation withdrawals

### Approval
- Graduation withdrawals require 3-of-4 approvals
- Parent approval is mandatory

### Destination
- Graduation payout destination must be a Student + Parent joint SAFE
- EOAs are prohibited as graduation payout destinations

### Emergency / Hardship
- Emergency proposals may be created only by Parent or Trustee
- Emergency withdrawals require 4-of-4 approvals

---

## Step 4 — Validate Guard Enforcement

Perform a basic validation pass:

- Attempt outbound transfer before graduation eligibility → should fail
- Attempt transfer to an EOA destination → should fail
- Attempt configuration changes in LOCKED state → should fail
- Confirm Parent approval requirement is enforced

If any prohibited action succeeds, the vault is not compliant.

---

## Step 5 — Lock Configuration

When entering LOCKED:

- Confirm signer set is final
- Confirm module set is final
- Confirm guard enforcement is active

After LOCKED, operators must not modify governance without formal signer approval.

---

## Step 6 — Graduation Execution (Standard Path)

At graduation eligibility:

1. Create withdrawal proposal
2. Collect 3 approvals (Parent required)
3. Execute as Parent or Trustee
4. Confirm transfer destination = Student + Parent joint SAFE

---

## Required Recordkeeping

For each vault, record:

- Safe address
- Network
- Signer addresses and mapped roles
- Graduation year / eligibility reference
- Enabled modules and guard policies
- Date vault entered LOCKED

---

## Final Note

Operators facilitate setup only.  
Governance belongs to signers.  
Enforcement belongs to code.

---

**Status:** Canonical Operator Template

