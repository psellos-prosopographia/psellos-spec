# Psellos Prosopographical Specification

This repository provides JSON-first, contract-only schemas and controlled vocabularies for a
SNAP:DRGN–aligned prosopographical data model, plus a clearly separated extension namespace for
Psellos-specific requirements.

## Project Purpose

The goal is to define a minimal, forward-compatible specification for representing people,
relationships, sources, and temporal scope, without prescribing any application implementation.
These contracts are intended to support consistent data exchange and validation across future
Psellos tooling.

## Project Context

The broader Psellos initiative is coordinated in the `psellos-hub` repository, while this
repository is the upstream authority for the canonical schemas, vocabularies, and specification
text that other implementations must follow.

## v0.1.0 Minimal Spec

v0.1.0 includes:
- a `persons` array of core person entities
- an `assertions` array of relationships
- the `parent_of` predicate
- an explicit `extensions` namespace stub for Psellos

v0.1.0 does not include yet:
- events or event modeling
- places or geographic modeling
- disputes or conflicting assertions
- de facto/de jure distinctions or other legal framing
- narrative layers or jurisdictional/right extensions

## Files

- [`schema/minimal.person-parent.v0.1.json`](schema/minimal.person-parent.v0.1.json)
- [`vocab/relationship-types.v0.1.json`](vocab/relationship-types.v0.1.json)
- [`examples/minimal.person-parent.v0.1.json`](examples/minimal.person-parent.v0.1.json)

## Relationship to SNAP:DRGN

The core schemas align conceptually with SNAP:DRGN by modeling people as entities, statements as
assertions grounded in sources, and temporal information as explicit ranges. RDF/OWL compatibility
is conceptual only and not required at this stage.

## Core vs. Extension Philosophy

- **Core (SNAP-aligned):** The `schema/core.snap.v0.1.json` file defines foundational contracts
  for persons, assertions, sources, and time ranges. Core vocabularies live under `vocab/` and are
  intentionally conservative to maximize interoperability.
- **Psellos Extensions:** The `schema/extensions.psellos.v0.1.json` file introduces a separate
  namespace for Psellos-specific concerns such as narrative layers, jurisdictional framing, and
  de facto/de jure distinctions. Extensions reference core definitions but do not alter them.

This separation allows the core specification to stay stable and broadly compatible while enabling
Psellos to capture additional interpretive context when needed.
