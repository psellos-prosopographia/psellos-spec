# Agent Guidelines

- This repository defines contracts only (schemas, vocabularies, spec documents).
- Do not add application code, build logic, or UI concerns.
- Keep core SNAP-aligned concepts separate from Psellos extensions.
- Any breaking change requires a new version entry in CHANGELOG.md.
- Do not edit other repositories from this context.

## Governance Authority

You are operating inside a subordinate `psellos-*` repository.

This repository is governed by the canonical authority defined in:

https://raw.githubusercontent.com/psellos-prosopographia/psellos-hub/main/AUTHORITY_INDEX.yml

Your role:
- Treat `psellos-hub` as the cross-repository authority for governance, coordination, and synchronization.
- Use the AUTHORITY_INDEX to understand:
  - what this repository is responsible for
  - what it is not responsible for
  - how to report status, milestones, and completed work upstream
- Follow raw GitHub URLs referenced by the hub as canonical navigation points when clarification is required.

Constraints:
- Do not invent governance rules or redefine authority locally.
- Do not assume this repository is the source of truth for shared schemas, IDs, or conventions unless explicitly stated.
- If there is uncertainty, defer to psellos-hub or report the uncertainty explicitly.

You may explore any raw GitHub URLs referenced in the AUTHORITY_INDEX as needed to understand structure, scope, and expectations.
