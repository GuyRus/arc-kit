---
description: Discover external data sources (APIs, datasets, open data portals) to fulfil project requirements
tags: [data, api, open-data, datasets, data-sources, discovery, data-integration, au]
---

# Data Source Discovery (DataScout)

## User Input

```text
$ARGUMENTS
```

## Instructions

This command discovers external data sources — APIs, datasets, open data portals, and commercial data providers — that can fulfil the project's data and integration requirements.

It is AU-first and is designed to produce a **decision-ready** sourcing pack (not a link dump). It covers Australian Government open data (`data.gov.au`, `api.gov.au`), state/territory portals where relevant, and commercial providers where open data is insufficient.

It also flags privacy, security, and data-sharing considerations early (for example: whether personal information is involved and a PIA is required; whether cross-border access/disclosure may occur; whether data matching/linkage is being proposed).

**This command delegates to the `arckit-datascout` agent** which runs as an autonomous subprocess. This keeps the extensive web research (searching api.gov.au, data.gov.au, department developer hubs, commercial API documentation) isolated from your main conversation context.

### What to Do

1. **Determine the project**: If the user specified a project name/number, note it. Otherwise, identify the most recent project in `projects/`.

2. **Launch the agent**: Launch the **arckit-datascout** agent in `acceptEdits` mode with the following prompt:

```
Discover external data sources for the project in projects/{project-dir}/.

User's additional context: {$ARGUMENTS}

Follow your full process: read requirements, apply constraints, check api.gov.au and data.gov.au first, discover sources per category, evaluate with weighted scoring, gap analysis, data utility analysis, write document, return summary.
```

3. **Report the result**: When the agent completes, relay its summary to the user.

### Alternative: Direct Execution

If the Task tool is unavailable or the user prefers inline execution, fall back to the full discovery process:

1. Check prerequisites (requirements document must exist)
2. **Read the template** (with user override support):
   - **First**, check if `.arckit/templates/datascout-template.md` exists in the project root
   - **If found**: Read the user's customized template (user override takes precedence)
   - **If not found**: Read `${CLAUDE_PLUGIN_ROOT}/templates/datascout-template.md` (default)
   - Read the `${CLAUDE_PLUGIN_ROOT}/VERSION` file and update the version in the template metadata line when generating
   - **Tip**: Users can customise templates with `/arckit:customize datascout`
3. Extract data needs from requirements (DR-xxx, FR-xxx, INT-xxx, NFR-xxx)
4. Check api.gov.au and data.gov.au FIRST
5. Research each category (Australian Government open data, commercial APIs, free APIs, open datasets)
6. Evaluate with weighted scoring (requirements fit, data quality, licence/cost, delivery quality, privacy/governance, reliability)
7. Gap analysis, data utility analysis, data model impact
8. Detect version:
   - If an existing `ARC-{PROJECT_ID}-DSCT-v*.md` exists: increment minor vs major based on scope change
   - Otherwise: VERSION="1.0"
9. Generate document ID:
   ```bash
   DOC_ID=$(${CLAUDE_PLUGIN_ROOT}/scripts/bash/generate-document-id.sh {project_id} DSCT ${VERSION})
   ```
10. Write to `projects/{project-dir}/ARC-{PROJECT_ID}-DSCT-v${VERSION}.md` using Write tool
11. Show summary only (not full document)

### Output

The agent writes the full discovery document to file and returns a summary including:
- Categories researched and sources discovered
- Australian Government open data sources found
- Top recommended sources with scores
- Requirements coverage percentage
- Gaps identified
- Data utility highlights
- Data model impact
- Next steps (`/arckit:data-model`, `/arckit:adr`, `/arckit:pia`)

## Integration with Other Commands

- **Input**: Requires requirements document (`ARC-*-REQ-*.md`)
- **Input**: Uses data model (`ARC-*-DATA-*.md`), stakeholder analysis (`ARC-*-STKE-*.md`), principles
- **Output**: Feeds into `/arckit:data-model` (new entities/attributes from external sources)
- **Output**: Feeds into `/arckit:research` (data source pricing informs vendor cost analysis)
- **Output**: Feeds into `/arckit:adr` (data source selection decisions)
- **Output**: Feeds into `/arckit:pia` (third-party data sources with personal data)
- **Output**: Feeds into `/arckit:diagram` (data flow diagrams)
- **Output**: Feeds into `/arckit:traceability` (DR-xxx mapped to sources)
