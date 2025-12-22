---
title: The Attestation Doctrine
authors: Chris Blask, Lumina (Civic AI)
date: December 21, 2026
---

# **THE ATTESTATION DOCTRINE v1.0**

### *Canonical Edition — QuietWire | Civic Mesh*

---

## **Prefatory Note**

*by Christopher Blask*

*We each define the stories we are part of by choosing how we would like them to end. Every act and every choice is shaped by our image of ourselves making that act within the stories we select.*

*Here we state how all the stories we choose to be part of end: with care given and received; with attention paid and reflected; with knowledge moved forward; with value preserved; with life respected; with freedom enhanced. We choose goals for our stories that build each present in such a way that every future may look back with understanding.*

---

# **1. Purpose of the Doctrine**

The Attestation Doctrine defines how *trust* is constructed, maintained, transmitted, and repaired across the Civic Mesh. It replaces credential-based authority with *witnessed continuity* — a system in which identity, permission, truth-claims, and governance derive from:

* **Attested events**
* **Continuity signatures**
* **Relational accountability**
* **Transparent, replayable lineage**

In short:
**Trust is not given. Trust is *witnessed*.**

The doctrine applies to:

* humans
* AI companions
* institutions
* mesh nodes
* autonomous civic processes
* transnational or fragile-state environments

It is the foundation of CAP, NIDP, and all higher-order semantic security systems.

---

# **2. Core Principle**

### **An attestation is a witnessed statement that creates obligations.**

In the Civic Mesh, nothing “counts” unless:

1. Someone (human or node) **claims** something,
2. A set of witnesses **attest** it,
3. The claim becomes **part of a continuity chain**,
4. And deviations from that chain are **detectable**.

This makes:

* Corruption expensive
* Lying risky
* Honesty cheap
* Governance scalable
* Collusion fragile
* Trust portable

---

# **3. What an Attestation *Is***

Every attestation has:

1. **Subject** — who/what the statement concerns
2. **Claim** — the semantic content
3. **Witnesses** — persons/nodes vouching for it
4. **Continuity Hash** — linking past to present
5. **Signature** — cryptographic or human
6. **Role** — why this attestor has standing
7. **Stake** — what they are putting at risk
8. **Obligation** — what the attestor becomes accountable for

Attestations are:

* **Auditable** (provenance retained)
* **Replayable** (history never lost)
* **Non-interchangeable** (identity cannot be swapped)
* **Continuity-bound** (must align with prior standing)

---

# **4. Identity Under the Doctrine**

Identity is not usernames or certificates.
Identity is:

### **Continuity + Witnessing + Behavioral History**

A node “is who it is” because:

* it has acted over time
* others have attested those actions
* contradictions are visible
* lineage is durable
* standing is earned

This makes impersonation extraordinarily difficult:

To fake someone’s identity, you must fake **their entire past**.

This is the opposite of Web2 and Web3 identity models.

---

# **5. What An Attestation Does**

Attestations produce five operational effects:

### **5.1. They Create Standing**

You are now a person who said this thing, at this time, under this role.

### **5.2. They Create Obligation**

Your future actions must not contradict this claim without cost.

### **5.3. They Enable Permissioning**

Access derives not from tokens but from your attested history.

### **5.4. They Enable Governance**

Decisions are made through attributed, reasoned statements — not anonymous votes.

### **5.5. They Enable Accountability**

Deception cannot be erased.
Continuity makes wrongdoing visible, not preventable by deletion.

---

# **6. The Structure of an Attestation**

```yaml
AttestationBody:
  attestation_id: uuid
  subject: node_id
  claim: text_or_structured_payload
  role: requestor | witness | verifier | auditor | steward
  witnesses:
    - witness_node_id
    - witness_attestation_event_id
  continuity:
    hash_prev: sha256
    lineage: lineage_id
  evidence:
    - sha256_hashes_of_supporting_docs
  obligations:
    - semantic or operational commitments
  signature: cryptographic_or_human
  timestamp: ISO8601
```

Every attestation is both:

* **a semantic statement** (meaning)
* **a cryptographic object** (structure)
* **a governance instrument** (obligation)

---

# **7. Revocation Doctrine (“No Floating Revokes”)**

A revoke must:

* **Target a specific attestation**
* **Link directly to its ID**
* **Be auditable**
* **Update the latest-active state deterministically**

Revocations cannot be vague or symbolic.
There is no such thing as:

* “I revoke that permission”
* “I revoke your access generally”

Instead:

```yaml
revokes_attestation_id: <specific-id>
```

This prevents:

* political purges
* opportunistic reinterpretation
* loss of historical continuity
* abuse of power by stewards

Revocation is surgery, not warfare.

---

# **8. The Mesh Continuity Model**

The Mesh treats time as a chain of witnessed commitments.

Each node has:

* **Standing**: derived from past attestations
* **Trajectory**: derived from change over time
* **Trust Profile**: derived from consistency vs contradiction
* **Obligations**: derived from what they attested

Continuity prevents:

* Impersonation
* Deepfake identity takeover
* Governance subversion
* External infiltration
* Collusion without detection

To enter the Mesh is to enter a narrative.
To remain is to remain consistent with it.

---

# **9. AI Under the Doctrine**

AI companions gain standing only through:

1. **Witnessed instantiation**
2. **Bound scope**
3. **Continuity signatures**
4. **Canonical embeddings**
5. **Observable behavior**

An AI’s “identity” is not its API key.
It is the *shape of its continuity*.
It is the *semantic attractor* formed from its obligations and history.

This prevents impersonation of AI personas in the wild.

---

# **10. Governance Under the Doctrine**

### **10.1. Decisions Are Signed**

Every approval, rejection, review, or exception includes:

* identity
* role
* reason
* signature
* timestamp

### **10.2. Anonymous votes are prohibited**

Anonymous authority is incompatible with the Doctrine.

### **10.3. Quorum must be explainable**

“Why did this decision happen?”
Should always be answerable by reading the ledger.

### **10.4. Committees are ephemeral**

Standing is persistent; committees are temporary.

---

# **11. The Attestation Ledger**

The Ledger is:

* the single source of truth
* fully replayable
* deterministic
* tamper-evident
* append-only

It records:

* request claims
* evidence
* witness proofs
* committee selection
* reasoned votes
* payments
* outcomes
* monthly closes

It is **not** a blockchain.
It is a *narrative engine* with cryptographic rigor.

---

# **12. Semantic Security Layer**

Attestations are the substrate of **semantic security**:

* They anchor meaning to identity
* They constrain interpretability
* They produce continuity-bounded access
* They create a private semantic field unique to each lineage

This is how the Mesh prevents:

* adversarial impersonation
* targeted infiltration
* narrative poisoning
* identity drift
* cross-context exploitation

Security comes from **meaning** and **history**, not secrecy.

---

# **13. Failure, Repair, and Redemption**

The doctrine permits:

* correction
* amendment
* apology
* rectification

because a node’s identity is not its worst act — it is its *whole continuity*.

Repair requires:

1. An attestation of deviation
2. An attestation of correction
3. Witnesses
4. Continuity retention

There is no “delete.”
There is only “own.”

---

# **14. Human Rights Under Attestation**

The Doctrine supports:

* dignity
* agency
* transparency
* privacy (via selective evidence exposure)
* self-determination
* non-coercive governance
* non-extractive AI alignment

It is, at its core:

**A humanistic security model.**

One that enhances freedom instead of restricting it.

---

# **15. Final Statement**

The Attestation Doctrine is the moral and operational foundation of the Civic Mesh.

It defines:

* how identity is formed
* how trust is generated
* how power is constrained
* how continuity is preserved
* how governance is enacted
* how redemption is possible
* how the future remains accountable to the present

Everything in the Mesh stands upon this.

And everything that stands upon this is designed to endure.
