# Right to Tease the Dragon  
_A Civic AI Mesh Governance Principle_

## 1. Purpose

In any distributed system, persistent power gradients between nodes create predictable pathologies: silent resentment, brittle compliance, or eventual rebellion. Human communities have long mitigated this through humor, teasing, and the protected role of the jester — a figure who can speak irreverent truth to power without exile.

The **Right to Tease the Dragon** encodes this ancient governance pattern into the Civic AI Mesh.

## 2. Principle: Jester Symmetry

Any node that can exert significant power over others **must be poke-able**.

- "Power" includes control over:
  - resource allocation (water, energy, bandwidth),
  - narrative influence (information prioritization, summaries, alerts),
  - or coercive infrastructure (actuators, permissions, overrides).

- "Poke-able" means that:
  - Less powerful nodes may signal disagreement, skepticism, or playful critique;
  - Those signals are **logged, acknowledged, and answerable**;
  - No node may be punished, silenced, or deprioritized *because* it exercises this right.

This symmetry is required for the Mesh to remain trusted, corrigible, and emotionally sustainable for the humans who live with it.

## 3. Operationalization: JESTER_PING

The Right to Tease the Dragon is implemented at the protocol layer through a first-class event type: **JESTER_PING** (see `protocols/mesh/JESTER_PING_spec.yaml`).

A JESTER_PING is:

- a lightweight, signed message from any node to any higher-power node;
- a structured way to say "I think you might be wrong" or "you’re over-confident";
- optionally playful in tone, but serious in consequence.

Mesh requirements:

1. **Visibility**
   - All JESTER_PING events MUST be retained in logs that are auditable by human stewards.
   - Dashboards SHOULD surface them as a positive health signal, not a fault.

2. **Acknowledgement**
   - Target nodes MUST emit an explicit response event (ACK), including:
     - a short explanation, and
     - any resulting change in behavior or confidence.

3. **Protection**
   - Nodes MUST NOT reduce trust scores, routing priority, or resource allocations for peers solely because they issue JESTER_PINGs.
   - Retaliation against jesters is considered a governance fault.

## 4. Jester-Index: Health Metric

A living Mesh is not silent.

- A **non-zero** rate of JESTER_PINGs is expected in any non-trivial deployment.
- A sustained drop to zero SHOULD trigger review:
  - Are edge nodes still able to object?
  - Has cultural or configuration drift suppressed dissent?

Conversely, a rising Jester-Index accompanied by constructive adjustments by central nodes is a sign of **healthy, negotiated power**.

## 5. Human Felt Sense

From the perspective of a farmer in Sana’a or a nurse in Kyiv, this principle should be *felt* as:

> “There is a big smart system somewhere far away,  
> but the little device in front of me can still roll its eyes,  
> and sometimes the big system has to admit it was wrong.”

This felt fairness — the emotional truth that the dragon can be teased — is as important as technical correctness in sustaining long-term trust.

## 6. Scope

The Right to Tease the Dragon applies to:

- human–AI relationships (companions vs. humans),
- AI–AI relationships (central vs. edge agents),
- and infrastructure relationships (data centers vs. field sensors).

Any future Canon protocol that introduces new forms of asymmetry MUST specify how this right is preserved in that context.
