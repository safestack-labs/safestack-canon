# SafeStack Canon Verification Guide

This document explains **how to verify the authenticity and integrity of SafeStack canonical documents**.

The canon protects SafeStack from silent modification, coercion, or unauthorized changes.

---

## 1. What Is Canonical

The canonical authority is the **cryptographically signed document**:

- `CANON_HASHES.md.asc`

If there is a conflict between files:
- `.asc` **always overrides** `.md`

---

## 2. Requirements

- GnuPG (GPG)
  - Linux / macOS: usually preinstalled
  - Windows: https://gnupg.org/download/

No private keys are required to verify the canon.

---

## 3. Verification Procedure

Run the following command in the directory containing the file:

```bash
gpg --verify CANON_HASHES.md.asc
```

---

## 4. Expected Output

Successful verification will show:

```
Good signature from "<Canonical Signer>"
```

Possible warning:

```
WARNING: not a detached signature
```

This warning is **expected** and **not an error**.
It appears because the canon uses **clear-signed documents**.

---

## 5. Interpretation Rules

- ✅ **Good signature** → Canon is authentic
- ❌ **Bad signature / No signature** → Canon is invalid
- ⚠️ "Not certified" warning → Normal if signer is not in your trust network

Only the signature validity matters.

---

## 6. What This Verification Guarantees

If verification succeeds, you know that:

- the canon was not modified
- the document integrity is intact
- the SafeStack principles are preserved

---

## 7. What Verification Does NOT Do

Verification does not:
- execute any code
- grant permissions
- authorize control
- imply trust beyond document integrity

---

## 8. Canon Rules

- Canonical documents are **never edited**
- Changes require:
  - new version
  - new hash
  - new signature
- Old versions remain archived

---

## Final Statement

> If the signature is valid, the canon stands.
> If the signature is broken, the canon is void.

This verification protects SafeStack **even from its creators**.

*End of Canon Verification Guide*

