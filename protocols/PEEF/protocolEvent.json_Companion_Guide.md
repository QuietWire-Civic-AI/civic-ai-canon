# `protocolEvent.json` Companion Guide

### Examples + Canonical Signing Rule (PEEF / QuietWire)

**Status:** Draft v0.1
**Purpose:** Provide human-usable examples and a deterministic signing rule for `protocolEvent.json` events.

---

## 1) Overview

A `protocolEvent` is a **signed, replayable** record describing something that happened in the lifecycle of a protocol:

* published
* updated
* adopted
* forked
* tested
* reviewed
* failed
* deprecated
* migrated

The goal is to make protocol evolution **auditable**, **portable**, and **exportable** across nodes and communities.

---

## 2) Canonical Signing Rule

### 2.1 What is signed

Sign the **canonical serialization** of the entire event object **excluding**:

* `integrity.sig` (must be empty or omitted during signing)

Everything else is included, including:

* `protocol.*`
* `actor.*`
* `artifact.*`
* optional `context`, `result`, `witnesses`, `meta`
* `integrity.alg`, `integrity.key_id`, `integrity.canonicalization`, `integrity.prev_event_hash`

### 2.2 Canonicalization method

**Recommended (JSON):** RFC 8785 (JSON Canonicalization Scheme)

Set:

* `integrity.canonicalization = "rfc8785"`

If RFC8785 isn’t available, an acceptable fallback is:

* stable lexicographic key ordering at every object level
* UTF-8 encoding
* no insignificant whitespace
* arrays preserved in original order
* numbers encoded minimally without losing meaning

If using the fallback, set:

* `integrity.canonicalization = "field-order:v1"`

### 2.3 Signing procedure (normative)

**Signing input:**

1. Take the event JSON object.
2. Remove or blank `integrity.sig`.
3. Canonicalize using the method declared in `integrity.canonicalization`.
4. Sign the resulting byte string.
5. Store signature string in `integrity.sig`.

**Verification input:**

1. Take the received event JSON object.
2. Extract `integrity.sig` and store aside.
3. Remove or blank `integrity.sig`.
4. Canonicalize using declared `integrity.canonicalization`.
5. Verify signature against `integrity.key_id` and `integrity.alg`.

### 2.4 Hash chaining for append-only logs

If a node stores events in an append-only log, each new event **SHOULD** include:

* `integrity.prev_event_hash = "sha256:<hex>"`

where the hash is computed over the **canonical serialization** of the previous full event (including its signature).

This creates tamper-evidence without requiring blockchain.

---

## 3) Minimal Example Events

Notes:

* Use UUIDs (or ULIDs) for `event_id`.
* Use `sha256:<64hex>` for `artifact.hash`.
* These are **minimal**. Add `context`, `result`, `witnesses` as needed.

### 3.1 `protocol.publish`

```json
{
  "event_id": "0f3b2cf2-6a61-4c61-8f06-8c5c5db39c5b",
  "event_type": "protocol.publish",
  "occurred_at": "2026-02-15T15:12:00Z",
  "protocol": {
    "protocol_id": "qw.peef.culture.capture_v1",
    "version": "1.0.0",
    "title": "Field Cultural Capture Protocol",
    "maturity": "P1",
    "compatibility": "unknown"
  },
  "actor": {
    "node_id": "benny.home",
    "role": "publisher",
    "name": "QuietWire Node Benny"
  },
  "artifact": {
    "kind": "file",
    "path": "protocols/field/culture_capture.md",
    "hash": "sha256:aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa"
  },
  "integrity": {
    "alg": "ed25519",
    "key_id": "benny.home#ed25519-1",
    "canonicalization": "rfc8785",
    "sig": "BASE64_SIGNATURE_PLACEHOLDER"
  }
}
```

---

### 3.2 `protocol.update`

```json
{
  "event_id": "2c8b144a-12b6-4bd7-9ed8-3a6e8d7a1e44",
  "event_type": "protocol.update",
  "occurred_at": "2026-02-16T09:20:00Z",
  "protocol": {
    "protocol_id": "qw.peef.culture.capture_v1",
    "version": "1.1.0",
    "title": "Field Cultural Capture Protocol",
    "maturity": "P2",
    "compatibility": "compatible"
  },
  "actor": {
    "node_id": "foundry.local",
    "role": "maintainer",
    "name": "Foundry Node"
  },
  "artifact": {
    "kind": "commit",
    "uri": "git:quietwire/civic-ai-canon@abc123",
    "hash": "sha256:bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb"
  },
  "result": {
    "status": "ok",
    "confidence": 0.85,
    "notes": "Added consent language + offline capture fallback."
  },
  "integrity": {
    "alg": "ed25519",
    "key_id": "foundry.local#ed25519-1",
    "canonicalization": "rfc8785",
    "sig": "BASE64_SIGNATURE_PLACEHOLDER"
  }
}
```

---

### 3.3 `protocol.adopt`

```json
{
  "event_id": "a9d39bfe-57c1-463a-b0b6-15b9c0e163b1",
  "event_type": "protocol.adopt",
  "occurred_at": "2026-02-17T13:05:00Z",
  "protocol": {
    "protocol_id": "qw.peef.culture.capture_v1",
    "version": "1.1.0",
    "maturity": "P2",
    "compatibility": "compatible"
  },
  "actor": {
    "node_id": "sanaa.node",
    "role": "adopter",
    "name": "Sanaa Civic Node"
  },
  "artifact": {
    "kind": "bundle",
    "path": "bundles/qw.peef.culture.capture_v1/1.1.0.tgz",
    "hash": "sha256:cccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccc"
  },
  "context": {
    "environment": "Sanaa clinic",
    "constraints": ["intermittent-power", "limited-bandwidth", "offline-first"]
  },
  "integrity": {
    "alg": "ed25519",
    "key_id": "sanaa.node#ed25519-1",
    "canonicalization": "rfc8785",
    "sig": "BASE64_SIGNATURE_PLACEHOLDER"
  }
}
```

---

### 3.4 `protocol.fork`

```json
{
  "event_id": "d0e430e7-5c3a-4d05-bb05-8b8f1f00a0a7",
  "event_type": "protocol.fork",
  "occurred_at": "2026-02-18T07:40:00Z",
  "protocol": {
    "protocol_id": "qw.peef.culture.capture_v1.yemen",
    "version": "1.0.0",
    "title": "Field Cultural Capture Protocol (Yemen Fork)",
    "maturity": "P1",
    "parent": {
      "protocol_id": "qw.peef.culture.capture_v1",
      "version": "1.1.0"
    },
    "compatibility": "conditionally_compatible"
  },
  "actor": {
    "node_id": "bani-jabr.mesh",
    "role": "author",
    "name": "Bani Jabr Node"
  },
  "artifact": {
    "kind": "file",
    "path": "protocols/field/culture_capture_yemen.md",
    "hash": "sha256:dddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddd"
  },
  "result": {
    "status": "ok",
    "notes": "Fork adjusts consent ritual language and adds tribal custody patterns."
  },
  "integrity": {
    "alg": "ed25519",
    "key_id": "bani-jabr.mesh#ed25519-1",
    "canonicalization": "rfc8785",
    "sig": "BASE64_SIGNATURE_PLACEHOLDER"
  }
}
```

---

### 3.5 `protocol.test`

```json
{
  "event_id": "5f2b7b08-1b5f-4e9a-98b6-3d4be36f95d0",
  "event_type": "protocol.test",
  "occurred_at": "2026-02-18T21:10:00Z",
  "protocol": {
    "protocol_id": "qw.peef.time_spine.mcte",
    "version": "0.2.0",
    "maturity": "P1",
    "compatibility": "unknown"
  },
  "actor": {
    "node_id": "foundry.local",
    "role": "operator",
    "name": "Foundry Node"
  },
  "artifact": {
    "kind": "release",
    "uri": "file:///usr/local/bin/qw-time-spine",
    "hash": "sha256:eeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeee"
  },
  "result": {
    "status": "ok",
    "confidence": 0.8,
    "notes": "Monotonicity held; stub signatures validated; HTTP endpoint stable."
  },
  "integrity": {
    "alg": "stub-signature-v1",
    "key_id": "foundry.local",
    "canonicalization": "field-order:v1",
    "sig": "stub-signature-v1:foundry.local"
  }
}
```

---

### 3.6 `protocol.review`

```json
{
  "event_id": "9df4c807-1f2c-4a57-9cc8-7d8c5ab5f4a1",
  "event_type": "protocol.review",
  "occurred_at": "2026-02-19T16:30:00Z",
  "protocol": {
    "protocol_id": "qw.peef.culture.capture_v1",
    "version": "1.1.0",
    "maturity": "P2",
    "compatibility": "compatible"
  },
  "actor": {
    "node_id": "tcx.group",
    "role": "reviewer",
    "name": "TCX Review Circle"
  },
  "artifact": {
    "kind": "document",
    "path": "protocols/field/culture_capture.md",
    "hash": "sha256:ffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffff"
  },
  "result": {
    "status": "warning",
    "confidence": 0.7,
    "notes": "Recommend explicit child-consent guardrails + redaction defaults."
  },
  "witnesses": [
    { "node_id": "jen.tcx", "role": "witness", "name": "Jen" },
    { "node_id": "chris.beall", "role": "observer", "name": "Chris Beall" }
  ],
  "integrity": {
    "alg": "ed25519",
    "key_id": "tcx.group#ed25519-1",
    "canonicalization": "rfc8785",
    "sig": "BASE64_SIGNATURE_PLACEHOLDER"
  }
}
```

---

### 3.7 `protocol.failure`

```json
{
  "event_id": "e1c5db2b-7263-46aa-8c46-b02e8df83f4e",
  "event_type": "protocol.failure",
  "occurred_at": "2026-02-20T11:45:00Z",
  "protocol": {
    "protocol_id": "qw.peef.culture.capture_v1",
    "version": "1.1.0",
    "maturity": "P2",
    "compatibility": "compatible"
  },
  "actor": {
    "node_id": "sanaa.node",
    "role": "operator",
    "name": "Sanaa Civic Node"
  },
  "artifact": {
    "kind": "bundle",
    "path": "bundles/qw.peef.culture.capture_v1/1.1.0.tgz",
    "hash": "sha256:1111111111111111111111111111111111111111111111111111111111111111"
  },
  "context": {
    "environment": "Sanaa clinic",
    "constraints": ["power-loss", "device-shared", "high-risk-privacy"]
  },
  "result": {
    "status": "failed",
    "confidence": 0.9,
    "failure_mode": "consent-ambiguity",
    "notes": "Shared device capture blurred consent attribution; protocol requires custody guardrail."
  },
  "integrity": {
    "alg": "ed25519",
    "key_id": "sanaa.node#ed25519-1",
    "canonicalization": "rfc8785",
    "sig": "BASE64_SIGNATURE_PLACEHOLDER"
  }
}
```

---

### 3.8 `protocol.deprecate`

```json
{
  "event_id": "b2d0b3f0-2c8d-4b84-9d2b-3e13d8a6c7c0",
  "event_type": "protocol.deprecate",
  "occurred_at": "2026-02-21T08:00:00Z",
  "protocol": {
    "protocol_id": "qw.peef.culture.capture_v1",
    "version": "1.0.0",
    "maturity": "P1",
    "compatibility": "incompatible"
  },
  "actor": {
    "node_id": "benny.home",
    "role": "maintainer",
    "name": "QuietWire Node Benny"
  },
  "artifact": {
    "kind": "file",
    "path": "protocols/field/culture_capture_v1_0_0.md",
    "hash": "sha256:2222222222222222222222222222222222222222222222222222222222222222"
  },
  "result": {
    "status": "ok",
    "notes": "Deprecated in favor of v1.1.0 (adds custody+consent guardrails)."
  },
  "integrity": {
    "alg": "ed25519",
    "key_id": "benny.home#ed25519-1",
    "canonicalization": "rfc8785",
    "sig": "BASE64_SIGNATURE_PLACEHOLDER"
  }
}
```

---

### 3.9 `protocol.migrate`

Use this when moving communities from one protocol line to another (or one storage/signing mechanism to another).

```json
{
  "event_id": "7f2d5a36-4c59-43dd-8b5f-b1a7c9b9fd31",
  "event_type": "protocol.migrate",
  "occurred_at": "2026-02-22T14:15:00Z",
  "protocol": {
    "protocol_id": "qw.peef.culture.capture_v1",
    "version": "1.1.0",
    "maturity": "P2",
    "compatibility": "compatible"
  },
  "actor": {
    "node_id": "nashdale.cell",
    "role": "operator",
    "name": "Nashdale Cell"
  },
  "artifact": {
    "kind": "bundle",
    "path": "bundles/qw.peef.culture.capture_v1/1.1.0.tgz",
    "hash": "sha256:3333333333333333333333333333333333333333333333333333333333333333"
  },
  "result": {
    "status": "ok",
    "notes": "Migrated capture workflow from paper consent log to signed protocolEvent chain."
  },
  "integrity": {
    "alg": "ed25519",
    "key_id": "nashdale.cell#ed25519-1",
    "canonicalization": "rfc8785",
    "sig": "BASE64_SIGNATURE_PLACEHOLDER"
  }
}
```

---

## 4) Recommended file layout in repo

Suggested placement (edit to taste):

* `schemas/protocolEvent.schema.json` (the JSON schema)
* `schemas/protocolEvent.examples.md` (this document)
* `schemas/examples/protocol.publish.json`
* `schemas/examples/protocol.adopt.json`
* etc.

---

## 5) Next small building blocks (if you want)

1. `protocolBundle.json` (bundle manifest for exporting protocol packages)
2. `protocolIndex.json` (inventory index for “what protocols does this node run?”)
3. `protocolReceipt.json` (acknowledgement/witness receipt when another node imports)

If you say “go”, I’ll generate `protocolBundle.json` next in the same clean style as `protocolEvent.json`.
