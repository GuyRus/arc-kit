# Data Source Discovery Guide (via `/arckit.datascout`)

`/arckit.datascout` discovers and evaluates external data sources (APIs, datasets, registries, and commercial providers) to fulfil project requirements.

For Australian Government contexts, it prioritises:
- `api.gov.au` (Australian Government API directory)
- `data.gov.au` (Australian open data catalogue)

It then expands to domain regulators/agencies, state/territory portals, and commercial providers where required.

## Prerequisites

| Artefact | Why it matters |
|----------|----------------|
| `ARC-<id>-REQ-v*.md` | Source of DR/INT/NFR constraints (fields, freshness, residency, latency, budget) |
| `ARC-<id>-DATA-v*.md` (recommended) | Lets discovery map sources to entities/attributes and identify model gaps |
| `ARC-<id>-STKE-v*.md` (recommended) | Identifies data consumers, quality expectations, and governance roles |

## Command

```bash
/arckit.datascout Discover data sources for <project>
```

Output: `projects/<id>/ARC-<id>-DSCT-vX.Y.md`

## What “Good” Looks Like (AU-first)

A useful DataScout output is not a list of links; it is a decision-ready pack:
- Data needs inventory extracted from requirements (DR/INT)
- Evidence-based evaluation cards per source (coverage, quality, terms, cost, delivery model)
- Comparison matrices and a ranked shortlist with scores
- Gap analysis with realistic options (collect internally, negotiate sharing, use proxies)
- Data model impact (new entities/attributes; sync strategy)

## Privacy, Security, and Data-Sharing Checks

Data sourcing often introduces privacy and governance obligations. DataScout should explicitly flag:
- Whether the source contains personal information or sensitive information (trigger `/arckit.pia`)
- Whether cross-border disclosure/access is likely (APP 8)
- Whether data matching/linkage is occurring (requires appropriate governance)
- Whether the security classification and handling constraints are compatible with the intended architecture (PSPF/ISM alignment)

## Linkages

- `/arckit.data-model` to incorporate selected sources into entities, attributes, and flows.
- `/arckit.adr` to record why a source was selected and what trade-offs were accepted.
- `/arckit.pia` when personal information is involved (especially if using third-party sources).
- `/arckit.risk` to record sourcing and reliance risks.
- `/arckit.diagram` to document external flows.
