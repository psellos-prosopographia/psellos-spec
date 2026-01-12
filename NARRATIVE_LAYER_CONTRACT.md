# Narrative Layer Contract (Psellos Extensions)

This document defines the schema-constrained contract for narrative layer metadata in Psellos extensions. It is scoped to describing what the data **is** (field names, types, and placement) rather than how tooling uses it.

## Normative: schema contract

### `extensions.psellos.layer`

- **Location:** `assertion.extensions.psellos.layer` in `schema/core.snap.v0.1.json`.
- **Type:** string.
- **Namespace:** flat (no hierarchical semantics implied).
- **Default:** `canon` when tooling needs a fallback.
- **Scope:** extension-only (no SNAP core semantics are asserted by this field).

No additional narrative-layer semantics are defined here beyond the schema constraints above.

## Non-normative: workflow integration

The Psellos workflow layers narrative content through M4–M6, including freezing, citations, and publication bundling. These behaviors are tooling-level integrations and **not** normative constraints of this contract.

- For freeze hash semantics, citation/reference workflows, and publication bundles, see `REVIEW_PUBLICATION_WORKFLOW.md`.
- For the interpretation of narrative identifiers and citation formats, see `REVIEW_PUBLICATION_WORKFLOW.md` and/or `ROADMAP.md`.
- Citation formats (e.g., BibTeX/CSL) and publication packages are tooling-level constructs; they are not required or validated by the spec.

### Optional M4 artifacts (extension-scoped)

The following artifacts may be produced by tooling and are **optional**:

- `layers_meta.json`: descriptive metadata about narrative layers and their provenance.
- `layer_stats.json`: summary statistics about assertions grouped by layer.

These artifacts are extension-scoped and do not change the schema contract.

## Non-normative: guarantees for downstream tooling

Downstream tooling should be able to derive deterministic exports (e.g., stable package outputs) from core artifacts and extension fields without inferring additional semantics beyond what the schema provides. Any workflow-specific interpretation (layer freezes, citation resolution, or bundle composition) should come from the referenced workflow documents rather than this contract.
