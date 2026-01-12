# Psellos Prosopographical Specification

This repository provides JSON-first, contract-only schemas and controlled vocabularies for a
SNAP:DRGN–aligned prosopographical data model, plus a clearly separated extension namespace for
Psellos-specific requirements.

## Project Purpose

The goal is to define a minimal, forward-compatible specification for representing people,
relationships, sources, and temporal scope, without prescribing any application implementation.
These contracts are intended to support consistent data exchange and validation across future
Psellos tooling.

## Relationship to SNAP:DRGN

The core schemas align conceptually with SNAP:DRGN by modeling people as entities, statements as
assertions grounded in sources, and temporal information as explicit ranges. The project remains
JSON-first and does not require RDF/OWL serialization at this stage.

## Core vs. Extension Philosophy

- **Core (SNAP-aligned):** The `schema/core.snap.v0.1.json` file defines foundational contracts
  for persons, assertions, sources, and time ranges. Core vocabularies live under `vocab/` and are
  intentionally conservative to maximize interoperability.
- **Psellos Extensions:** The `schema/extensions.psellos.v0.1.json` file introduces a separate
  namespace for Psellos-specific concerns such as narrative layers, jurisdictional framing, and
  de facto/de jure distinctions. Extensions reference core definitions but do not alter them.

This separation allows the core specification to stay stable and broadly compatible while enabling
Psellos to capture additional interpretive context when needed.
