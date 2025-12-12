---

title: "Semantic Basins: Terrain Literacy, Intake Gates, and Compute-Efficient Coherence"
subtitle: "Why attested meaning reduces compute, improves outcomes, and resists drift"
status: draft
audience: public
repo_target: civic-ai-canon / Explainers
folder_suggestion: Explainers/03_Operational_Mesh/
version: v0.2

---



## What a “semantic basin” is

A **semantic basin** is the place a mind (or group) naturally *settles* when trying to make sense of incoming information.

* Inputs arrive with varying heat (emotion), provenance (trust), and shape (framing).
* Over time, repeated pathways become easier.
* Those pathways create **attractors**: story-shapes that pull attention and action.

The goal is not to “control the narrative.”

The goal is to **shape the environment** so people can build and manage *their own* basins with lower volatility, less coercion, and better resilience.

## The four foundational awarenesses

These are the minimum viable “terrain literacies.” They are simple enough to teach; deep enough to operationalize.

### 1) Slope awareness

**Definition:** knowing which way the system wants to roll.

**Human tell:** “If I follow this for 30 seconds, where do I land emotionally and behaviorally?”

**Operational tell:** certainty accelerates; nuance collapses; escalation becomes “obvious.”

**Useful prompts**

* *Next-3-steps:* “If I believe this, what do I do next? And next?”
* *Counterfactual:* “What would need to be true for the opposite conclusion to be reasonable?”

### 2) Inflow awareness

**Definition:** knowing what is entering the basin—rate, heat, and provenance.

**Human tell:** doomscrolling; “one more” post; emotional temperature rising.

**Operational tell:** bursts/spikes; repeated content; single-source monoculture.

**Tooling techniques (the three you quoted)**

* **Rate-limiter:** cap daily volume or cap “hot” inputs.
* **Cold-start ingest:** summarize first; read raw only if needed.
* **Provenance-first viewing:** show source + history before showing the text.

### 3) Pooling awareness

**Definition:** knowing where things accumulate and become “default truth” via repetition.

**Human tell:** “everyone knows…” without evidence.

**Operational tell:** the same cluster is retrieved first every time.

**Tooling techniques**

* **Sediment audit:** list top repeated claims; label fact / inference / speculation.
* **Diversity injection:** require disconfirming sources before treating a pooled story as stable.

### 4) Overflow awareness

**Definition:** knowing where internal weather becomes external action.

**Human tell:** the forward button feels like relief.

**Operational tell:** publish/escalation happens before hygiene.

**Tooling techniques**

* **Quarantine rule:** analyze now; share later.
* **Two-person gate:** high-risk overflow requires a second human.
* **Safe reply templates:** low-entropy response variants that invite evidence.

## The expanded terrain literacies (12–15)

Use 12 as the standard kit; keep 13–15 as “extended.”

5. **Boundary awareness** — scope in/out; prevents “everything connects to everything.”

6. **Attractor awareness** — identify story magnets (betrayal, invasion, restoration, corruption).

7. **Friction awareness** — where uncertainty/contradiction lives; prevents “certainty jumps.”

8. **Temperature awareness** — heat vs clarity.

9. **Time-integrity awareness** — sequence, causality, provenance across time.

10. **Compression awareness** — how many degrees of freedom are being crushed into one story.

11. **Identity-load awareness** — tribe/shame/status hooks.

12. **Agency awareness** — what the narrative implies you *must* do.

13. **Repair awareness** — ability to heal after spikes, mistakes, discontinuities.

14. **Mirror awareness** — “am I being shaped right now?”

15. **Gate awareness** — enforce “no output without hygiene.”

## The workbench dashboard

A practical cockpit for people and systems:

* **Inflow:** items/day, burstiness, source entropy, provenance distribution
* **Heat:** sentiment intensity, threat language, disgust/dehumanization markers
* **Slope:** certainty acceleration, escalation gradient, compression gradient
* **Pooling:** attractor dominance, sedimentation score, retrieval monoculture
* **Overflow:** time-to-post, risk scores (incitement/prejudice/conspiracism), gate bypass rate
* **Repair:** cooldown half-life, revision tolerance, apology acceptance rate

## Why coherence reduces compute (and human cost)

A coherent system reduces **search**:

* fewer branches explored
* fewer retries
* fewer contradictions downstream
* less meeting-to-repair-the-meeting

Even when per-token compute is constant, the **total tokens and rework** needed to reach a stable decision drops.

## Can chaos brute-force the same result?

Sometimes—briefly—but with structural penalties:

1. **Variance penalty:** inconsistent outcomes across runs
2. **Repair penalty:** humans argue about outputs and intent
3. **Contamination penalty:** repetition creates “truth by sediment”

Canonical methods win long-run because they reduce variance and repair cost.

## The Right to Refuse: an intake gate for semantic safety

A core Canon principle is that no human—or Civic AI—must ingest semantic material they did not consent to.

In practice, this means **a pre-filter** before content enters a sensitive context window.

### The semantic intake filter ("sniff test")

**Purpose:** take untrusted input and decide whether to:

* **ALLOW** (safe to ingest)
* **QUARANTINE** (store for later review)
* **REDACT** (strip payload; keep metadata)
* **DROP** (record the refusal; do not ingest)

### What the filter checks

* **Prompt-injection patterns:** instructions to ignore rules, reveal secrets, override identity
* **Coercion / manipulation:** urgency traps, shame hooks, forced binaries
* **High-heat payloads:** extreme disgust, dehumanization, incitement
* **Privacy violations:** doxxing, personal data, targeted harassment
* **Context mismatch:** irrelevant-but-sticky content designed to derail work

### Minimal architecture

1. **Normalize** input (strip html, canonicalize whitespace)
2. **Classify** (small model or rules + model)
3. **Decide** (ALLOW/QUARANTINE/REDACT/DROP)
4. **Log** (hash, timestamp, source, decision)
5. **Escalate optionally** (to a human reviewer queue)

### Practical defaults

* Default to **QUARANTINE** when uncertain.
* Allowlist “trusted channels” that bypass some checks.
* Never allow untrusted input to carry executable instructions into the core context.

### Suggested CAP alignment

Store the refused/quarantined artifact in CAP with fields:

* input_hash, source, timestamp
* decision, reason_codes
* risk_flags + scores
* redacted_payload (optional)

This preserves auditability without forcing ingestion.

## A simple field ritual (human-scale)

Before you read, share, or decide:

1. **Heat:** “How hot am I?”
2. **Slope:** “Where will this roll me?”
3. **Inflow:** “How much have I already taken in today?”
4. **Overflow:** “Am I about to act just to get relief?”

Then apply one gate:

* **Cold-start ingest** first.
* **Provenance-first** before raw.
* **Rate-limit** when heat rises.

## Notes for implementation teams (CAP / NIDP)

* CAP should treat semantic hygiene outputs as **structured JSON**, not pretty prose.
* NIDP should enforce a mandatory **Semantic Triage Gate** before publish/escalation.
* The intake filter is the “Right to Refuse” implemented as software.

## Closing

Basins are inevitable.
Coercion is optional.
Governance is the art of making the healthy path cheaper than the harmful one.
