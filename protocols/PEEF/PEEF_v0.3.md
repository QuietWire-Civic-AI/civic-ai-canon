---
title: Protocol Evolution & Export Framework 
author: Lumina, Bone
date: 15 February, 2026
---

# PEEF

## Protocol Evolution & Export Framework

**A Canonical method for growing, validating, exporting, forking, and operationalizing protocols across a distributed mesh**

**Status:** Draft v0.3
**Intended users:** Civic AI nodes, human stewards, operators, NGOs, infrastructure teams, governance councils
**Primary outcome:** A repeatable pipeline that turns local learning into shareable “operational RNA.”

---

## 0. Purpose

PEEF defines how a protocol moves from:

**Local improvisation → Local ritual → Stable procedure → Exportable bundle → Adopted standard → Living lineage**

It exists to solve one core problem:

> Good protocols die in local notebooks.
> Bad protocols spread in glossy PDFs.

PEEF makes the good ones portable **without centralizing control**.

---

## 1. Definitions

### 1.1 Protocol

A repeatable method that reliably produces an outcome in a specific environment.

Protocols can be:

* technical (API format, signing method, monitoring loop)
* operational (incident response routine, procurement flow)
* cultural (attestation ritual, boundary declaration, storytelling norms)
* governance (decision thresholds, conflict resolution, legitimacy checks)

### 1.2 Node

Any actor able to:

* execute protocols
* record outcomes
* export artifacts

Nodes may be:
humans, groups, institutions, or AI companions.

### 1.3 Canon

An append-only memory fabric that:

* stores protocol artifacts
* stores evolution history
* binds decisions to evidence
* enables replay

PEEF assumes Canon exists (or a minimal substitute: signed logs + hash chaining).

### 1.4 Exportable bundle

A package that another node can adopt **without needing the origin node’s presence**.

---

## 2. Core principles

### 2.1 Local autonomy is non-negotiable

Protocols may be shared, but adoption is voluntary and context-bound.

### 2.2 Evidence beats charisma

A protocol becomes exportable because it **works**, not because a famous person said it does.

### 2.3 Drift is expected

Protocols will mutate. PEEF makes drift visible and safe.

### 2.4 Forking is legitimate

Forking is not betrayal. It is how protocols adapt without central control.

### 2.5 Minimal viable interoperability

Protocols must specify:

* inputs
* outputs
* boundary conditions
* failure modes
* required attestations

---

## 3. The lifecycle ladder

A protocol’s maturity is defined by the highest rung it satisfies.

### P0 — Spark

* A pattern noticed in the wild.
* “We did a thing and it worked once.”

**Required artifact:** `Protocol_Spark.md` (or log entry)

* context
* what happened
* why it seemed to work
* immediate risks

---

### P1 — Repeatable

* Works at least **3 times** in the same context.
* Has a named procedure.

**Required artifacts:**

* `Protocol_Steps.md` (explicit steps)
* `Inputs_Outputs.md`

---

### P2 — Stable

* Works across **at least two operators** (or two shifts, two teams).
* Failure modes are known.
* Has rollback.

**Required artifacts:**

* `Failure_Modes.md`
* `Rollback_Procedure.md`
* `Operator_Checklist.md`

---

### P3 — Exportable

* Works in **at least one additional node** (another org, another community, another site).
* Includes a “minimum install kit.”
* Has provenance + versioning.

**Required artifacts:**

* `Export_Bundle/` directory
* `README_Adoption.md`
* `Compatibility.md`
* `Attestation_Template.md`

---

### P4 — Institutionalizable

* Adoption does not require the originating node to evangelize.
* Can be embedded into policy, training, or vendor products.

**Required artifacts:**

* `Policy_Language.md`
* `Training_Module.md`
* `Audit_Criteria.md`

---

### P5 — Living Lineage

* Multiple forks exist.
* Compatibility boundaries are clear.
* Evolution is tracked like a family tree.

**Required artifacts:**

* `Lineage_Map.md`
* `Fork_Registry.md`
* `Interoperability_Contracts.md`

---

## 4. The minimal export bundle format

Every P3+ protocol SHOULD ship as:

```
ProtocolName/
  README_Adoption.md
  Spec.md
  Steps.md
  Inputs_Outputs.md
  Failure_Modes.md
  Rollback.md
  Attestation_Template.md
  Compatibility.md
  Examples/
  Reference_Implementations/   (optional)
  Test_Cases/                  (optional)
  CHANGELOG.md
  SIGNATURES/                  (optional but recommended)
```

### 4.1 README_Adoption.md MUST include

* What this protocol is for
* Who should NOT adopt it
* Minimum prerequisites
* Time-to-first-value
* Safety notes
* How to ask for help (without dependency)

---

## 5. Versioning and identity

PEEF uses **semantic versioning** with a slightly stricter rule:

* **MAJOR**: breaks compatibility, changes outputs or guarantees
* **MINOR**: adds capability, preserves compatibility
* **PATCH**: fixes errors, clarifies text, no behavior change

Every export bundle MUST include:

* `protocol_id` (stable)
* `version`
* `origin_node`
* `timestamp`
* `license / sharing terms`

Recommended `protocol_id` format:
`qw.peef.<family>.<name>`

Example:
`qw.peef.governance.funding_transparency`

---

## 6. Forking protocol

Forks are expected. They must be legible.

### 6.1 Fork declaration MUST include

* parent protocol_id + version
* reason for fork
* what changed
* intended compatibility stance:

  * **compatible**
  * **conditionally compatible**
  * **incompatible**

### 6.2 Fork artifact format

`Fork_Declaration.md` plus an attested log entry.

---

## 7. Attestation requirements

### 7.1 What must be attested

At minimum, PEEF expects attestation for:

* protocol publication (who published, when)
* version changes
* adoption events
* incident/failure events
* forks
* deprecation

### 7.2 Minimal attestation structure (MUST)

* `event_type`
* `protocol_id`
* `version`
* `node_id`
* `hash_of_bundle_or_doc`
* `signature` (or MAC)
* `witnesses` (optional)
* `notes`

This is what turns “a PDF” into **evidence.**

---

## 8. Evaluation metrics

A protocol is considered “good” when it produces:

### 8.1 Reliability

* repeatability under constraints
* low operator variance

### 8.2 Safety

* bounded failure modes
* rollback exists
* harms are visible

### 8.3 Portability

* minimal dependencies
* clear prerequisites
* understandable by a new operator

### 8.4 Legibility

* can be read and followed by humans
* can be executed/checked by machines

### 8.5 Non-centralization

* adoption does not create dependency on origin node
* forking is allowed
* local sovereignty preserved

---

## 9. Protocol “fitness tests”

A protocol may graduate from P2 → P3 only if it passes these tests.

### Test A: Cold operator test

A competent operator unfamiliar with the protocol can execute it from the bundle.

### Test B: Drift tolerance test

The protocol still works if:

* one input source changes
* a dependency fails
* the environment is partially degraded

### Test C: Failure clarity test

A failure produces:

* a recognizable signal
* an actionable next step
  Not mystery.

### Test D: Export integrity test

The exported protocol can be verified:

* hash matches
* signature verifies
* version is explicit

---

## 10. Deprecation protocol

Protocols sometimes must die cleanly.

A protocol MAY be deprecated if:

* a safer replacement exists
* it introduces unbounded harm
* it cannot be maintained

Deprecation MUST include:

* replacement pointer
* migration advice
* end-of-life date (if relevant)

Artifact:
`DEPRECATED.md` + attested entry.

---

## 11. How PEEF propagates

Propagation happens via **three channels**:

### 11.1 Human-to-human transfer

Workshops, mentorship, operator exchanges.

### 11.2 Canon bundle transfer

Bundles exported as:

* GitHub directories
* signed archives
* QR-codes / USB drops for offline

### 11.3 Service-mediated discovery

QuietWire can offer:

* registry indexing
* compatibility hints
* search and lineage visualization

But crucially:
The service must not become the chokepoint.

---

## 12. QuietWire implementation hooks

If we’re mapping this to product reality:

### 12.1 Registry

* searchable protocol index
* by domain, maturity, dependencies, language

### 12.2 Lineage graph

* visualize forks
* show compatibility edges

### 12.3 Adoption telemetry (opt-in)

* nodes can publish anonymous adoption attestations
* lets the mesh see what is spreading

### 12.4 Protocol “linting”

Automated checks:

* required files present
* version syntax correct
* attestation references valid

---

## 13. Immediate next steps for us

To make PEEF real, quickly:

1. Create a `protocols/peef/` folder in Canon
2. Commit this as `PEEF_v0.3.md`
3. Apply PEEF to 1–2 existing protocols (Hand, Time Spine, IOF) as exemplars
4. Create the first `Fork_Declaration.md` template
5. Create a “Protocol Export Bundle Generator” script (even crude)

---

## 14. Closing: the evolutionary frame

Civilization evolves through **replicable patterns**.

PEEF is not a bureaucratic overlay.

It is the thing that lets a good local idea become a shared immune response, without demanding a king.

---

If you want, next turn I can produce:

* a **one-page “PEEF for humans”** (executive version)
* a **machine-readable schema** for the attestation events (`protocol_event.json`)
* a **bundle template directory** you can drop directly into GitHub as a starter kit
