---
name: interf-update-canonical
description: >
  Fetch the latest canonical dependency types from the interf-labs/canonical-dependencies
  repository. Use when you want the most up-to-date types for declaring contracts or
  previewing rollouts. The bundled types may be behind the latest version.
---

# Update Canonical Dependencies

Fetch the latest canonical dependency types from the live repository.

## When to Use

- Before declaring a contract for a new or niche sector
- When a canonical type you expect is missing from the bundled version
- When you want the most current type definitions, systems, and sector patterns

## Instructions

1. **Fetch the index** to see all available types:

   Use WebFetch to get: https://raw.githubusercontent.com/interf-labs/canonical-dependencies/main/types/index.md

2. **Fetch specific category overviews** as needed:

   - https://raw.githubusercontent.com/interf-labs/canonical-dependencies/main/types/integration/overview.md
   - https://raw.githubusercontent.com/interf-labs/canonical-dependencies/main/types/auth/overview.md
   - https://raw.githubusercontent.com/interf-labs/canonical-dependencies/main/types/data/overview.md
   - https://raw.githubusercontent.com/interf-labs/canonical-dependencies/main/types/infrastructure/overview.md
   - https://raw.githubusercontent.com/interf-labs/canonical-dependencies/main/types/stakeholder/overview.md
   - https://raw.githubusercontent.com/interf-labs/canonical-dependencies/main/types/process/overview.md

3. **Fetch specific type details** when you need the full definition:

   Pattern: `https://raw.githubusercontent.com/interf-labs/canonical-dependencies/main/types/{category}/{type}.md`

   Examples:
   - `types/integration/crm/README.md` — CRM base definition
   - `types/integration/crm/systems/salesforce.md` — Salesforce-specific
   - `types/integration/crm/sectors/healthcare.md` — Healthcare sector patterns

4. **Use the fetched types** in place of the bundled canonical-dependencies when declaring or previewing.

## Note

The bundled types in the `agent-onboarding-protocol` skill are a stable snapshot. This skill fetches the live, latest version which may include new types, systems, and sectors added by community contributions and agent research loops.
