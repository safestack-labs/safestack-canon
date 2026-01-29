# SafeStack Architecture Map v2

## 0. Purpose
This document defines the **canonical architecture** of the SafeStack ecosystem.
It describes *what exists*, *what is allowed*, and *what must never exist*.

SafeStack is **not** a centralized system.
It is a **federation of autonomous nodes** bound by ethics, not commands.

---

## 1. Core Principle

> **Intention is allowed. Command is forbidden.**

No component in SafeStack has the authority to force execution on another.
All interactions are based on:
- voluntary disclosure
- local validation
- autonomous decision

---

## 2. System Layers (High Level)

```
Human
  ↓
Intention Layer (Telegram)
  ↓
Intention Ledger (GitHub / append-only)
  ↓
Autonomous Nodes (SafeStack NodeOS)
  ↓
Observer Layer (R2000 / Pi 5)
```

Each layer has **strictly limited rights**.
No layer may exceed its mandate.

---

## 3. Human Layer

The human does **not issue commands**.
The human expresses *intent*.

The system does not guarantee:
- execution
- response
- visibility

---

## 4. Intention Layer (Telegram Bot)

### Role
- Collect human intentions
- Remove personal identity
- Serialize intention as neutral data

### Explicit Non-Roles
- No execution
- No routing
- No enforcement

Output: `intention.json`

---

## 5. Intention Ledger

### Nature
- Append-only
- Public or semi-public
- Addressless

### Meaning
An intention in the ledger is **a fact, not a request**.

Nodes may:
- read
- ignore
- refuse

Nodes are never obligated.

---

## 6. Node Layer (SafeStack NodeOS)

### Node Properties
Each node:
- has an identity anchor
- validates a signed manifest
- enforces a canon
- maintains its own lifecycle

### Node Rights
A node may:
- accept an intention
- deny an intention
- ignore all intentions
- terminate its participation

### Node Prohibitions
A node may never:
- be remotely controlled
- reveal protected human identity
- obey forced central authority

---

## 7. Lifecycle States

- BORN
- ACTIVE
- LOCKDOWN
- SILENT
- TERMINATED

Transitions are **local only**.

---

## 8. Autonomy Severance (Layer 5)

**Terminology note:** this document intentionally avoids destructive language.

If a node detects:
- coercion
- physical tampering
- forced de-anonymization
- violation of canon

It may execute **Autonomy Severance**:
- identity invalidation
- trust context erasure
- voluntary termination

This is **not destruction**.
This is refusal to exist under violation.


---

## 9. Observer Layer (R2000 / Pi 5)

### Role
- Read-only observability
- Status aggregation
- Alert visualization

### Restrictions
- No write access
- No control paths
- No override capability

Observer exists to **see**, never to act.

---

## 10. Absolute Prohibitions

SafeStack must never contain:
- command-and-control channels
- forced execution paths
- remote kill switches
- recovery after autonomy severance

---

## 11. Final Assertion

SafeStack protects humans **even from itself**.

If the system must choose between:
- survival
- ethics

It chooses ethics.

---

*End of Architecture Map v2*

