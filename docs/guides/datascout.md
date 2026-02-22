# Data Source Discovery Guide (via `/arckit.datascout`)

`/arckit.datascout` discovers and evaluates external data sources (APIs, datasets, registries, and commercial providers) to fulfil project requirements.

It is AU-first, but the report structure is deliberately **generic and reusable**: it focuses on decision-ready artefacts (evidence, scoring, trade-offs, gaps), while aligning privacy and governance handling to Australian policy.

## Prerequisites

| Artefact | Why it matters |
|----------|----------------|
| `ARC-<id>-REQ-v*.md` | Source of DR/INT/NFR constraints (fields, freshness, residency, latency, budget) |
| `ARC-<id>-DATA-v*.md` (recommended) | Lets discovery map sources to entities/attributes and identify model gaps |
| `ARC-<id>-STKE-v*.md` (recommended) | Identifies intended users, quality expectations, and governance roles |

## Command

```bash
/arckit.datascout Discover data sources for <project>
```

Output: `projects/<id>/ARC-<id>-DSCT-vX.Y.md`

## What the Output Should Contain

A useful DataScout output is not a directory of links. It should provide:

1. **Data needs inventory** extracted from requirements (DR/INT) with minimum fields and constraints.
2. **Discovery log** (what was searched, when, and why) to make the process repeatable.
3. **Per-source evaluation cards** with evidence links (coverage, quality, terms, cost, delivery model).
4. **Comparison matrices** and a ranked shortlist with scores.
5. **Gap analysis** with realistic options (collect internally, negotiate sharing, use proxies).
6. **Data model impact** (new entities/attributes and sync strategy).
7. **Decision hooks**: which choices should become ADRs.

## AU Governance Alignment (Without Losing Generic Utility)

Data sourcing often creates privacy, security, and governance obligations. DataScout should explicitly flag (not assume):

- **Personal information / sensitive information**: triggers a PIA (`/arckit.pia`) and deeper controls.
- **Cross-border disclosure/access** (APP 8): supplier hosting/support patterns must be assessed.
- **Data matching / linkage**: requires careful governance and risk treatment.
- **Security classification constraints**: ensure handling/hosting remains compatible with PSPF/ISM expectations.

These flags are designed to keep the report generally useful while ensuring the project’s next steps align with Australian obligations.

## Suggested Workflow

```text
1. Run /arckit.requirements (if not already done)
2. Run /arckit.datascout
3. Review shortlist with data owners, privacy, security, and procurement
4. Record key selections as ADRs (/arckit.adr)
5. Update the data model (/arckit.data-model)
6. If personal information is involved, run /arckit.pia and address APP 8 where relevant
```

## Linkages

- `/arckit.data-model` to incorporate selected sources into entities, attributes, and flows.
- `/arckit.adr` to record why a source was selected and what trade-offs were accepted.
- `/arckit.pia` when personal information is involved (especially with third-party sources).
- `/arckit.risk` to record reliance, quality, and governance risks.
- `/arckit.diagram` to document external flows.
