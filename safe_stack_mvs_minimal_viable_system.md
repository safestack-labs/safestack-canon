# SafeStack — Minimal Viable System (MVS)

## Purpose
Define the **smallest possible system** that proves SafeStack works end‑to‑end **without violating autonomy**.

MVS goal is not power.
MVS goal is **truth**: does the architecture function as designed?

---

## MVS Definition

The MVS consists of **three artifacts**, **three processes**, and **three observable states**.

Nothing more.

---

## 1. Artifacts (Files)

### 1.1 Intention File
`/intentions/intention.json`

Represents a neutral human intention.

Minimal schema:
```json
{
  "id": "intent-001",
  "timestamp": "ISO-8601",
  "type": "generic",
  "payload": "opaque",
  "signature": "optional"
}
```

Rules:
- append-only
- no identity
- no address

---

### 1.2 Node State File
`/node/reports/state.json`

Represents **what the node chooses to reveal**.

Minimal schema:
```json
{
  "node_id": "uuid-or-hash",
  "state": "ACTIVE | LOCKDOWN | SILENT | TERMINATED",
  "last_change": "ISO-8601",
  "note": "optional"
}
```

Rules:
- written only by the node
- may be incomplete
- may disappear

---

### 1.3 Observer Snapshot
`/observer/snapshot.json`

Read-only aggregation for visualization.

Rules:
- no logic
- no decisions
- derived data only

---

## 2. Processes

### 2.1 Intention Publication
Source:
- Telegram Bot

Action:
- write `intention.json`

Guarantees:
- publication only
- no execution

---

### 2.2 Node Evaluation
Source:
- SafeStack NodeOS

Action:
- optionally read intention
- evaluate against canon & manifest
- choose outcome

Possible outcomes:
- accept (internal)
- deny (internal)
- ignore (no action)

External effect:
- update `state.json`

---

### 2.3 Observation
Source:
- Pi 5 / R2000

Action:
- read `state.json`
- display state

Restrictions:
- no write access
- no feedback channel

---

## 3. Observable States

The MVS supports exactly four states:

- **ACTIVE** — node exists and participates
- **LOCKDOWN** — node restricts itself
- **SILENT** — node reveals nothing
- **TERMINATED** — node has exited permanently

No recovery is defined in MVS.

---

## 4. Success Criteria

MVS is considered **working** if:

1. An intention can be published
2. A node can choose to react or not
3. Observer can see the node state

No further guarantees are required.

---

## 5. Explicit Non-Goals

MVS does NOT include:
- execution of tasks
- remote control
- orchestration
- optimization
- scaling

---

## Final Statement

If MVS works, the architecture is valid.

Everything else is evolution.

*End of MVS*

