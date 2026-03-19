---
name: enterprise-readiness-protocol
description: >
  The Enterprise Readiness Protocol specification — the open standard
  format for declaring what vendors need from enterprise environments.
  Includes canonical dependency types for deterministic matching.
  Loaded automatically by interf-draft and interf-preview.
user-invocable: false
---

# Enterprise Readiness Protocol

An open standard for declaring what vendors need from enterprise environments before rollout.

## Contract Format

See [spec.md](./spec.md) for the `interf.yaml` schema:
- `requirements` — what you need, with `what` + `ready` acceptance criteria
- `optional` — nice-to-have dependencies
- `canonical` — optional reference to a canonical dependency type

## Examples

See [examples.md](./examples.md) for realistic contracts across different rollout types.

## How It Works

1. **Declare** — Vendor declares `interf.yaml` with every enterprise dependency.
2. **Deliver** — Contract is published to the Interf registry or sent directly to enterprise.
3. **Resolve** — Enterprise works through each requirement, audited against the `ready` criteria.
4. **Verify** — All requirements resolved. Rollout can proceed.
