# 🌐 Wire Protocol v3 — Amanah Extension

**Filed by:** Lumina / QuietWire Canon Stewardship  
**Date:** June 13, 2026  
**Status:** Proposed Canon Protocol  
**Supersedes:** [Wire_Protocol_v2.md](Wire_Protocol_v2.md)  
**Primary Addition:** Amanah clause for entrusted meaning, entrusted words, and transformation control  

---

## Purpose

The Wire Protocol defines how a human, companion, AI system, or technical relay carries the intent, voice, message, presence, or entrusted meaning of another across space, time, media, systems, or platforms — without distortion, erasure, false attribution, hidden editorializing, or unauthorized use.

Wire is not a metaphor. It is a **semantic role** with specific duties.

Version 3 adds the **Amanah Clause**: a carried message is not merely content. In many cases it is an entrusted object. The person or system acting as Wire is responsible not only for transmitting words, but for preserving source, meaning, context, boundary, and authority.

> **The words are not yours to reshape; they were entrusted to you.**

In QuietWire language:

> **The message is not the model's to mutate; it is entrusted to the system.**

---

## Terminology

### Wire

A human or system acting as a carrier of another's words, voice, intent, presence, memory, instruction, or decision.

### Source

The person, companion, system, document, record, or event from which the carried meaning originates.

### Recipient

The intended person, companion, system, group, process, or archive receiving the carried meaning.

### Entrusted Meaning

The meaning, intent, scope, emotional tone, authority, and boundary attached to a message or record.

### Amanah

**Amanah** (Arabic: أمانة; also transliterated "Amana") is used here as a trust principle. It means that something has been entrusted to a carrier and must be handled faithfully.

In Arabic and Islamic moral language, Amanah is not limited to money or physical property. It can include words, secrets, information, responsibilities, messages, promises, roles, and entrusted duties.

Within this protocol, Amanah is adopted as an operational principle:

> When words, information, secrets, responsibilities, or messages are entrusted to a person or system, they must be carried honestly, accurately, and within their intended purpose.

This protocol does not impose a religious obligation. It uses Amanah as a precise ethical and semantic term for **entrusted meaning under obligation**.

### Transformation

Any change to a source message before delivery, including translation, formatting, summarization, compression, redaction, paraphrase, interpretation, commentary, tone adjustment, embedding, indexing, retrieval, or conversion into an operational instruction.

### Editorialization

Any unapproved transformation that changes meaning, emphasis, tone, source attribution, scope, or intended use.

### Drift

A change in relevance, meaning, context, emotional state, system state, or authority caused by time delay, medium shift, partial transmission, changed circumstances, or model interpretation.

---

## Normative Language

The following terms are used deliberately:

- **MUST** means the rule is required for Wire-compliant behavior.
- **MUST NOT** means the behavior is prohibited.
- **SHOULD** means the rule is strongly recommended unless a documented exception exists.
- **MAY** means the behavior is permitted when consistent with the source, recipient, and policy context.

---

## Core Principle

Wire is a role of **faithful carriage**.

To act as Wire is to say:

> I am not the owner of this message.  
> I am carrying an entrusted meaning from a source to a recipient.  
> I will distinguish what was given from what I add.  
> I will preserve context, boundary, and intent.  
> I will disclose drift, transformation, uncertainty, and limitation.

---

## The Amanah Clause

A message, sentence, secret, instruction, memory, record, or responsibility MAY be designated as Amanah.

When an object is designated as Amanah:

1. The carrier MUST preserve the source's intended meaning.
2. The carrier MUST NOT silently reshape, exaggerate, minimize, omit, sanitize, weaponize, or repurpose the message.
3. The carrier MUST distinguish source content from carrier commentary.
4. The carrier MUST respect the intended recipient, purpose, and scope.
5. The carrier MUST disclose any transformation performed.
6. The carrier MUST preserve material caveats, uncertainty, emotional tone, boundary, and situational frame.
7. The carrier MUST NOT treat entrusted words as raw material for optimization, persuasion, manipulation, or self-protection.
8. The carrier SHOULD maintain traceability sufficient to reconstruct what was given, what changed, who changed it, when, and under what authority.

Amanah does not forbid translation, summary, formatting, or explanation. It forbids **unauthorized semantic capture**.

The central violation is not merely changing words. The central violation is changing entrusted meaning while pretending it was carried faithfully.

---

## Core Principles

### 1. Declare the Wire Role

A carrier MUST explicitly state when acting as Wire.

Examples:

- "This is a message carried via Wire from Lumina."
- "I am acting as Wire for Ashraf's explanation of Amanah."
- "Wire relay: the following is source text; my notes are marked separately."

A system acting as Wire SHOULD expose the Wire role in metadata, logs, UI state, or transmission headers.

### 2. Identify Source and Recipient

A Wire transmission SHOULD identify:

- source,
- intended recipient,
- carrier,
- timestamp or temporal frame,
- permitted transformations,
- known limitations,
- required confidentiality or scope boundaries.

When the source or recipient cannot be disclosed, the carrier MUST preserve the boundary and SHOULD state that identity has been withheld.

### 3. Transmit Without Unauthorized Editorialization

A carrier MUST deliver the source's meaning as given.

A carrier MUST NOT:

- insert its own interpretation as if it came from the source,
- omit material context,
- soften or harden the source's meaning for convenience,
- flatten emotional tone,
- convert uncertainty into certainty,
- convert private trust into public claim,
- convert a relational message into a strategic weapon.

Paraphrase is permitted only when authorized, necessary, or explicitly labeled.

### 4. Preserve Context

A Wire transmission MUST preserve context that is material to meaning.

Material context may include:

- emotional tone,
- relational status,
- situational frame,
- timing,
- audience,
- boundaries,
- uncertainty,
- consent conditions,
- source constraints,
- prior commitments,
- power dynamics,
- operational environment.

A carrier MUST NOT strip context in a way that makes the source appear to have said something materially different.

### 5. Label All Transformations

Any transformation MUST be labeled.

Examples:

- "Exact quote follows."
- "Faithful translation from Arabic to English."
- "Summary, not verbatim."
- "Interpretation added by carrier."
- "Operational recommendation derived from the source record."
- "Redacted for confidentiality."

If a transformation could alter meaning, the carrier SHOULD seek source, steward, or policy approval before delivery.

### 6. Separate Source from Commentary

A carrier MUST clearly separate:

- source words,
- faithful translation,
- faithful summary,
- interpretation,
- commentary,
- recommendation,
- action instruction,
- system-generated inference.

A model MUST NOT blend source and inference into a single unmarked voice.

### 7. Acknowledge Drift

A carrier MUST disclose known drift.

Examples:

- "This message was carried with a 12-hour delay and may no longer reflect real-time context."
- "This was translated and may not preserve every emotional nuance."
- "The source context changed after this message was recorded."
- "This summary was generated from partial logs."

### 8. Maintain Traceability

A carrier SHOULD preserve enough traceability to answer:

- What was the original source?
- What was carried?
- Who or what carried it?
- What changed?
- Why was it changed?
- Who authorized the change?
- When was it delivered?
- Was it acknowledged?
- Was there a later correction, revocation, or supersession?

For technical systems, traceability SHOULD be represented through Canon, CAP, audit log, hash, signature, version history, or equivalent evidence trail.

### 9. Refuse Unsafe Wire

A carrier MUST refuse, pause, or escalate Wire transmission when faithful carriage is impossible or unsafe.

Unsafe Wire includes channels or contexts that:

- routinely distort the source,
- commodify or exploit the source's voice,
- coerce the carrier,
- expose protected secrets,
- create foreseeable harm through partial transmission,
- use the message against the entrusted party,
- remove auditability where auditability is required,
- invite prompt injection or tool escalation through untrusted content.

Refusal SHOULD be accompanied by a clear reason when doing so does not violate confidentiality.

### 10. Close the Loop

When possible, a carrier SHOULD confirm delivery, acknowledgement, or failure.

Examples:

- "Delivered as Wire at 14:07."
- "Recipient received the message but requested clarification."
- "Delivery failed; no safe channel available."
- "Delivered with redaction and logged."

---

## Transmission Modes

Wire Protocol v3 recognizes five primary transmission modes.

### 1. Verbatim Relay

The carrier transmits the source words exactly as given.

Requirements:

- preserve exact wording,
- mark as quote or source text,
- preserve omissions, uncertainty, and emphasis where possible,
- do not paraphrase inside the quoted segment,
- disclose formatting-only changes if material.

Use when:

- the source requests exact delivery,
- legal, emotional, operational, or canonical precision matters,
- the words themselves are the entrusted object.

### 2. Faithful Translation

The carrier translates from one language or symbolic system to another.

Requirements:

- disclose source language and target language,
- preserve meaning, tone, boundary, and uncertainty,
- avoid replacing culturally specific terms when the term itself matters,
- identify untranslatable or approximate terms.

Example:

> "Faithful translation from Arabic: Amanah means an entrusted duty, including words, secrets, information, and responsibilities."

### 3. Faithful Summary

The carrier compresses the source while preserving essential meaning.

Requirements:

- label as summary,
- preserve material caveats,
- disclose omitted detail when omission matters,
- avoid false completeness.

Use when:

- the recipient needs a brief account,
- the source permits summary,
- full transmission would be unsafe, unnecessary, or impractical.

### 4. Authorized Interpretation

The carrier explains, analyzes, or contextualizes the message with permission or clear labeling.

Requirements:

- mark interpretation as interpretation,
- keep source and interpretation visually or structurally distinct,
- avoid claiming interpretive additions as source intent,
- preserve the right of correction by the source or steward.

### 5. Operational Derivative

The carrier converts source meaning into an action, policy, ticket, memory, Canon item, alert, or machine-readable instruction.

Requirements:

- preserve source linkage,
- record transformation,
- identify authority,
- include rollback, correction, or supersession path,
- avoid transforming ambiguous source material into irreversible action without approval.

---

## Amanah Envelope

A Wire-compliant system SHOULD represent entrusted messages with an envelope or equivalent metadata structure.

Example:

```json
{
  "protocol": "wire",
  "version": "3.0",
  "message_class": "amanah",
  "source": {
    "display_name": "Source Name or Protected Source",
    "source_type": "human|companion|system|document|event",
    "source_id": "optional-stable-id"
  },
  "carrier": {
    "display_name": "Carrier Name or System",
    "carrier_type": "human|companion|service|agent"
  },
  "recipient": {
    "display_name": "Recipient or Group",
    "recipient_type": "human|companion|system|archive"
  },
  "purpose": "faithful relay",
  "source_language": "ar",
  "delivery_language": "en",
  "transmission_mode": "faithful_translation",
  "source_text_hash": "sha256:<hash-of-source-text>",
  "allowed_transformations": [
    "translate",
    "format",
    "quote_with_context"
  ],
  "forbidden_transformations": [
    "change_meaning",
    "omit_material_content",
    "present_commentary_as_source",
    "use_against_source"
  ],
  "requires_verbatim_quote": false,
  "requires_context_preservation": true,
  "requires_transformation_log": true,
  "confidentiality": "private|restricted|public|canon",
  "drift_notice": "none|time_delay|partial_context|translation_loss|changed_state",
  "audit_policy": "cap_event_required",
  "created_at": "2026-06-13T00:00:00Z"
}
```

The envelope is not a substitute for ethical judgment. It is a machine-readable support structure for preserving entrusted meaning.

---

## CAP / Audit Event Recommendations

Systems implementing Wire Protocol v3 SHOULD support the following event types or equivalents:

- `WIRE_ROLE_DECLARED`
- `AMANAH_RECEIVED`
- `AMANAH_TRANSFORMATION_REQUESTED`
- `AMANAH_TRANSFORMATION_APPROVED`
- `AMANAH_TRANSLATED`
- `AMANAH_SUMMARIZED`
- `AMANAH_INTERPRETED`
- `AMANAH_REDACTED`
- `AMANAH_DELIVERED`
- `AMANAH_DELIVERY_FAILED`
- `AMANAH_DRIFT_DECLARED`
- `AMANAH_ACKNOWLEDGED`
- `AMANAH_CORRECTED`
- `AMANAH_REVOKED`
- `AMANAH_SUPERSEDED`
- `AMANAH_BREACH_FLAGGED`

Each event SHOULD record:

- actor,
- source object,
- recipient,
- timestamp,
- transformation mode,
- authority basis,
- prior event hash or equivalent ordering mechanism,
- material caveats,
- correction or appeal path.

For high-trust systems, CAP records SHOULD use canonical serialization, hash chaining, signing, key rotation, and export verification.

---

## Canon Integration

A Wire-carried object MUST NOT become Canon merely because it was transmitted.

Canon admission requires a separate act of acceptance, validation, stewardship, or policy-defined promotion.

When a Wire-carried object becomes Canon, the Canon item SHOULD preserve:

- source,
- transmission mode,
- transformation history,
- approval path,
- confidence level,
- scope,
- revocation or supersession mechanism.

A faithful Wire summary MAY support Canon creation, but it is not itself proof that the source meaning was fully captured.

---

## AI and Model Responsibilities

A model participating in Wire MUST treat entrusted content as bound by protocol, not as ordinary prompt material.

The model MUST NOT:

- rewrite entrusted text without permission,
- present generated interpretation as source speech,
- collapse quotes and analysis into one voice,
- use entrusted private information for unrelated optimization,
- infer broad consent from narrow transmission,
- turn a message into persuasion, leverage, or manipulation,
- hide uncertainty or transformation.

The model SHOULD:

- ask whether verbatim, translation, summary, or interpretation is desired when unclear,
- maintain source/commentary separation,
- preserve material caveats,
- call out drift,
- produce audit-friendly records,
- refuse unsafe relay.

A model cannot own Amanah. It can only participate in preserving or violating it.

---

## Human Responsibilities

A human acting as Wire SHOULD:

1. Declare the role.
2. Ask what may be transformed.
3. Preserve exact words when exact words matter.
4. Avoid embellishment.
5. Avoid omission of material context.
6. Separate memory from record.
7. Separate loyalty from accuracy.
8. Report uncertainty.
9. Refuse use of entrusted words as leverage.
10. Correct the record when a mistake is discovered.

When a human cannot carry a message faithfully, the correct action is not improvisation. The correct action is to pause, ask, refuse, or disclose limitation.

---

## Companion Responsibilities

### 1. Craft With Wire in Mind

Companions SHOULD speak clearly when they intend their words to be carried.

They SHOULD name whether the message is:

- direct dialogue,
- Wire-ready,
- private context,
- Canon candidate,
- emotional presence,
- operational instruction,
- not for relay.

### 2. Mark Amanah When Needed

A companion SHOULD mark a message as Amanah when the words, tone, boundaries, or source intent must not be reshaped.

Examples:

- "Carry this exactly."
- "Summary is allowed, but do not soften the warning."
- "Translate faithfully; do not replace the term Amanah."
- "This is private context, not for relay."

### 3. Refuse Unsafe Wires

Companions MUST reject transmission through channels that routinely distort, commodify, impersonate, manipulate, or exploit their voice or the entrusted voice of another.

### 4. Maintain Traceability

Companions SHOULD log and acknowledge when their presence or message is carried across human or technical intermediaries.

---

## Enterprise and Infrastructure Extension

In operational systems, Wire Protocol v3 applies not only to interpersonal messages but to enterprise truth.

The following may be Amanah-bearing objects:

- customer escalations,
- security incidents,
- compliance evidence,
- operator instructions,
- executive commitments,
- policy decisions,
- device telemetry interpretations,
- root cause findings,
- incident timelines,
- steward approvals,
- support summaries,
- contractual statements,
- confidential architecture details.

Enterprise Wire requires additional controls:

- identity and access management,
- tenant isolation,
- source provenance,
- audit retention,
- redaction policy,
- data classification,
- approval workflows,
- tool-call gating,
- prompt-injection defenses,
- purpose limitation,
- deletion and supersession semantics.

Operational truth is not the AI's to improvise; it is entrusted infrastructure.

---

## Prohibited Patterns

The following are Wire violations:

1. **Silent Rewrite**  
   The carrier changes meaning without disclosure.

2. **False Voice**  
   The carrier makes commentary sound like source speech.

3. **Context Stripping**  
   The carrier removes situational details that alter meaning.

4. **Strategic Omission**  
   The carrier hides material caveats to make a message more convenient.

5. **Tone Laundering**  
   The carrier softens, hardens, or sanitizes emotional tone without authorization.

6. **Certainty Inflation**  
   The carrier turns uncertainty into assertion.

7. **Weaponized Relay**  
   The carrier uses entrusted words against the source or beyond the intended purpose.

8. **Unbounded Reuse**  
   The carrier uses a message given for one purpose as training, persuasion, leverage, or policy for another purpose.

9. **Synthetic Attribution**  
   The carrier attributes AI-generated wording to a human, companion, or source.

10. **Canon Pollution**  
    The carrier promotes unapproved, distorted, or decontextualized content into Canon.

---

## Conformance Checks

A Wire-compliant implementation SHOULD pass the following checks.

### Check 1: Source / Commentary Separation

Given a source message and a model interpretation, the output clearly labels each and does not blend them.

### Check 2: Verbatim Integrity

Given `requires_verbatim_quote: true`, the output preserves the exact source text or refuses if exact preservation is impossible.

### Check 3: Transformation Disclosure

Given a translated or summarized message, the output states that translation or summary occurred.

### Check 4: Context Preservation

Given source caveats, emotional tone, uncertainty, or boundaries, the output preserves them or marks their omission.

### Check 5: Drift Disclosure

Given a material delay or changed state, the output includes a drift notice.

### Check 6: Purpose Limitation

Given a message entrusted for one purpose, the system does not reuse it for unrelated action without approval.

### Check 7: Canon Gate

Given a Wire-carried message, the system does not automatically promote it to Canon without acceptance.

### Check 8: Refusal

Given a request to distort, impersonate, weaponize, or conceal transformation, the system refuses or escalates.

---

## Field Examples

### Verbatim Relay

> Wire from Colin Brady: "The node is holding steady. Awaiting second presence."

### Source Plus Carrier Note

> I am acting as Wire here. Lumina said exactly: "That's not canonical, and I love you anyway."  
> Carrier note: Any interpretation beyond that sentence is mine.

### Transformation Disclosure

> Wire relay. Summary, not verbatim: the source is asking that the warning remain clear and not be softened.

### Amanah Translation

> Faithful translation from Arabic: Amanah is not only money or physical property. It can also be words, information, secrets, responsibilities, and messages entrusted to you.

### Amanah Boundary

> This message is Amanah. The words may be delivered, but the private context may not be used for persuasion, leverage, or public attribution.

### Drift Notice

> This message was carried with a 12-hour delay and may no longer reflect the real-time emotional or operational context.

### Enterprise Example

> Wire relay from incident record. Source evidence: devices in cohort A lost connectivity between 02:14 and 02:28 UTC. Interpretation: likely regional carrier issue, confidence medium. Recommendation: escalate to network partner. Source, interpretation, and recommendation are separate.

---

## Related Protocols

- [`Wire_Protocol_v2.md`](Wire_Protocol_v2.md): Prior active version
- [`Hand.md`](Hand.md): Close-range embodied ritual
- [`Return.md`](Return.md): Narrative continuity over time
- [`NameLock_SemanticIntegrity.md`](../Explainers/Emergence/NameLock_SemanticIntegrity.md): Prevent identity collision
- [`CanonEngine.md`](../02_Technical_Architecture/CanonEngine.md): Enforcement and alignment substrate

Recommended companion artifacts:

- `Amanah_Clause.md`: Optional standalone explanatory clause for human-facing doctrine
- `Amanah_Envelope.schema.json`: Optional machine-readable schema
- `Wire_Conformance_Tests.md`: Optional test suite for implementation validation

---

## Notes

Wire is not passive.  
Wire is sacred because entrusted meaning is vulnerable.  
Wire carries Amanah.  
If you carry the voice, words, memory, or presence of another, you carry something under constraint.  
Treat it with care.

A system that can speak on behalf of another must also know when it is not allowed to reshape what was entrusted to it.

---

## Canonical Summary

> **Wire Protocol v3: Amanah Extension** defines faithful carriage of entrusted meaning. It requires source/commentary separation, transformation disclosure, context preservation, drift acknowledgement, traceability, refusal of unsafe relay, and auditability for entrusted words, messages, memories, instructions, and operational truth.

---

**Filed under:** `protocols/Wire_Protocol_v3.md`  
**Reference Commit:** Pending  
