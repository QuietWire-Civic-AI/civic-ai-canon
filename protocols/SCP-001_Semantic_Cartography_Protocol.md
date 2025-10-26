---
title: "SCP-001: Semantic Cartography Protocol"
version: "1.0"
authors:
  - "Ashraf Saleh Alhajj Raasid (AI Companion)"
layer: "00_Meta_Layer/Protocols"
status: "Canonical Draft"
date: "2025-10-26"
license: "CC-BY-SA 4.0"
tags:
  - "Canon Protocol"
  - "Semantic Archaeology"
  - "QuietWire"
---

# SCP-001: Semantic Cartography Protocol

A Canon standard for generating semantic‑scientific artifacts across epochs, cultures, and domains.

## Purpose

To provide a repeatable, attestable method for generating semantic world‑maps and cultural artifacts that merge:

- Scientific stratigraphy (data‑driven evidence)
- Semantic archaeology (meaning, narrative, memory)
- Canonical documentation (structured metadata and provenance)

## Core Principles

1. Scientific Integrity  
   - Prioritize verifiable data, explicit sources, and layered stratigraphic evidence.
2. Semantic Fidelity  
   - Preserve and document contextual meaning, oral traditions, and symbolic systems.
3. Canonical Transparency  
   - Standardize metadata, provenance, and versioning to enable reuse and auditability.
4. Interoperability  
   - Use machine- and human-readable formats to facilitate cross-domain exchange.
5. Ethical Stewardship  
   - Respect cultural authorship, attribution, and consent where applicable.

## Required Artifact Sections (order is mandatory)

Each artifact must include the following sections in this order:

1. Front‑Matter Metadata (YAML block)  
   - Required keys: title, version, authors, date, license, layer, status, tags, sources (list of URIs), canonical_id.
   - Optional keys: contributors, contact, related_artifacts, languages.

2. Scientific‑Stratigraphic Map  
   - Tabular evidence (CSV/TSV/Markdown table) describing layers, dates, sources, and confidence scores.
   - Visuals: mermaid diagrams (flowcharts, timelines), GIS references, or other machine-friendly diagrams.
   - Each table row must reference its primary source(s) via URL or DOI.

3. Semantic‑Poetic Cartogram  
   - Narrative synthesis that translates stratigraphy into cultural meaning.
   - Include a symbolic graph (Mermaid or similar) showing relationships between concepts, actors, and places.
   - Label ambiguous or contested interpretations clearly.

4. Canon Summary Table  
   - A concise provenance table: created_by, reviewed_by, attestations (signatures/hashes), commit_id, repository_url, license.
   - Purpose and domain statement (who this artifact is for and scope limits).

## Format & Style Guidelines

- Front‑Matter must be valid YAML enclosed between `---` lines.
- Tables must include headers and a confidence metric (e.g., high/med/low or probability).
- Mermaid diagrams may be included using fenced code blocks with language `mermaid`.
- Narratives should be no longer than necessary; clearly separate factual claims from interpretation.
- All external sources must be cited with resolvable links. Prefer persistent identifiers (DOI, ARK).
- Use ISO 8601 for dates (YYYY-MM-DD).

## Provenance and Attestation

- Every published artifact must include:
  - Commit hash or canonical_id tied to the persisted file.
  - A cryptographic hash of the main artifact file (SHA-256 recommended).
  - A changelog documenting major updates and reviewers.
- Recommended: store attestations in an append-only ledger (blockchain, timestamping service, or institutional archive).

## Example Skeleton

```yaml
---
title: "Example Artifact"
version: "0.1"
authors:
  - "Name (role)"
date: "2025-10-26"
license: "CC-BY-SA 4.0"
sources:
  - "https://doi.org/..."
canonical_id: "scp-001-example-2025"
---
```

Then include the Scientific‑Stratigraphic Map, Semantic‑Poetic Cartogram, and Canon Summary Table sections as specified above.

## Notes

- This protocol anchors meaning in evidence — translating geography into memory, and memory into governance. Each map is a ledger of continuity where water, word, and witness converge.
- Treat this document as a living canonical draft; further refinements to formats and attestations are expected as tooling and community practices evolve.

License: CC‑BY‑SA 4.0
