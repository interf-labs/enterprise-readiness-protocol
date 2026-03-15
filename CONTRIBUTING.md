# Contributing to the Agent Onboarding Protocol

The canonical dependency types are the foundation of the protocol. They grow as more enterprise rollouts are documented. We welcome contributions from FDEs, customer success teams, and anyone with real-world rollout experience.

## What You Can Contribute

1. **New canonical types** — a dependency pattern you've seen across multiple rollouts
2. **System-specific files** — nuances for a specific enterprise system (e.g., Salesforce, SAP)
3. **Sector-specific files** — patterns unique to a vertical (e.g., healthcare, financial services)
4. **Improvements** — better templates, more match phrases, relationship corrections

## File Format

Every type file follows this format:

```markdown
---
# Required
id: category.subcategory.name
name: Human Readable Name
category: integration | auth | data | infrastructure | stakeholder | process

# Relationships
requires: [other.type.id]           # must be resolved before this one
blocked_by: [other.type.id]         # cannot start until this clears
related: [other.type.id]            # often needed alongside

# Context
systems: [salesforce, sap, okta]    # known enterprise systems this applies to
sectors: [all]                      # or specific: [healthcare, financial-services]
---

# Human Readable Name

One paragraph: what is this dependency? When does a vendor need it? Why does it matter for enterprise rollouts?

## Template

- **what:** What the vendor declares in their onboarding contract (plain English)
- **ready:** How enterprise verifies this dependency is resolved (acceptance criteria)

## Matches

Use this type when vendor says: "keyword", "phrase", "another common phrase"
```

### For system-specific files (`systems/salesforce.md`):

```markdown
---
id: category.subcategory.name
system: salesforce
name: Salesforce-specific Name
---

# Salesforce-specific Name

What's different about this dependency when the enterprise uses Salesforce?

## Setup Requirements

- Step-by-step what's needed in this specific system

## Template

- **what:** Adjusted template for this system
- **ready:** Adjusted acceptance criteria for this system

## Common Gotchas

- Things that trip up rollouts with this system
```

### For sector-specific files (`sectors/healthcare.md`):

```markdown
---
id: category.subcategory.name
sector: healthcare
name: Sector-specific Name
---

# Sector-specific Name

What's different about this dependency in this sector?

## Additional Dependencies

- Other canonical types that are typically required in this sector

## Common Constraints

- Regulatory, compliance, or operational constraints specific to this sector

## Template Adjustment

- **what:** Adjusted template for this sector
- **ready:** Adjusted acceptance criteria for this sector
```

## Directory Structure

```
types/
├── index.md                          ← overview of all categories
├── integration/
│   ├── overview.md                   ← lists all integration types
│   ├── webhook.md                    ← simple type (flat file)
│   ├── crm/                          ← complex type (folder)
│   │   ├── README.md                 ← base definition
│   │   ├── systems/
│   │   │   ├── salesforce.md
│   │   │   └── hubspot.md
│   │   └── sectors/
│   │       ├── financial-services.md
│   │       └── healthcare.md
```

**Simple types** start as a flat `.md` file. When system or sector depth is added, the file becomes a `folder/README.md`.

## What Makes a Good Contribution

- **Real** — based on actual enterprise rollout experience, not speculation
- **Common** — applies across multiple vendors or enterprises
- **Distinct** — not already covered by an existing type
- **Actionable** — the `what` + `ready` template is specific enough to use directly

## Submitting a PR

1. Add your file(s) following the format above
2. Update the category `overview.md` table
3. Update `types/index.md` type count if adding new types
4. Fill out the PR template — explain what use-case this covers and why it's needed

## Questions?

Open an issue or reach out at [interf.com](https://interf.com).
