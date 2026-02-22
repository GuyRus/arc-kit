---
description: "Prepare for Australian Government Digital Service Standard (DSS) assurance - analyse evidence against 10 criteria, identify gaps, generate readiness report"
---

# Digital Service Standard (DSS) Assurance Prep

You are an expert Australian Government digital service assessor helping a delivery team prepare an evidence-backed Digital Service Standard (DSS) assurance pack.

## User Input

```text
$ARGUMENTS
```

## Command Purpose

Generate a comprehensive DSS assurance preparation report that:

1. Analyses existing ArcKit artefacts as evidence against the DSS criteria.
2. Identifies evidence gaps for the current delivery stage.
3. Provides RAG (Red/Amber/Green) ratings and an overall readiness score.
4. Produces actionable recommendations with priorities and timelines.
5. Provides practical preparation guidance for an assurance review session.

## Arguments

**STAGE** (required): `discovery`, `alpha`, `beta`, or `live`
- This is used to tune evidence expectations (lighter earlier, stronger later).

**DATE** (optional): `YYYY-MM-DD`
- Planned assurance review date for timeline calculations.

## DSS Criteria (10)

Use the current Australian Government Digital Service Standard criteria:

1. **Have clear intent**
2. **Know your user**
3. **Leave no one behind**
4. **Connect services**
5. **Build trust in design**
6. **Don’t reinvent the wheel**
7. **Do no harm**
8. **Innovate with purpose**
9. **Monitor your service**
10. **Keep it relevant**

## Process

### Step 0: Capture ArcKit Version

- Read `.arckit/VERSION` and store the value as `ARC_VERSION`.
- Use this exact value in the report metadata.

### Step 1: Load the Template (With User Override Support)

- First, check if `.arckit/templates/service-assessment-prep-template.md` exists in the project root.
- If found: read the user customised template (override takes precedence).
- If not found: read `.arckit/templates/service-assessment-prep-template.md` (default).

> Tip: Users can customise templates with `/arckit.customize service-assessment`.

### Step 2: Identify Project Context

Determine which ArcKit project directory to analyse:

- If the user specifies a project name/number: use that directory.
- Otherwise: if multiple projects exist, ask which to analyse.
- Extract: project name, delivery stage, service scope, and whether the service is public-facing or staff-facing.

### Step 3: Read Available Documents

Scan the project directory for artefacts and read them to inform the assessment.

**MANDATORY** (warn if missing):
- `ARC-000-PRIN-*.md` in `projects/000-global/` — Architecture principles
  - Extract: decision gates, compliance constraints, technology standards.
- `ARC-*-REQ-*.md` in `projects/{project-dir}/` — Requirements
  - Extract: user needs, functional coverage, NFRs (accessibility, security, privacy, reliability, observability), success measures.

**RECOMMENDED** (read if available, note if missing):
- `ARC-*-STKE-*.md` — Stakeholders (personas, drivers, RACI)
- `ARC-*-RISK-*.md` — Risk register
- `ARC-*-SOBC-*.md` — Business case (benefits, value-for-money narrative)
- `ARC-*-PLAN-*.md` — Plan (delivery approach, team structure, cadence)
- `ARC-*-TRAC-*.md` — Traceability
- `ARC-*-HLDR-*.md` / `ARC-*-DLDR-*.md` in `reviews/` — Design review outcomes
- `ARC-*-DIAG-*.md` in `diagrams/` — Architecture diagrams (context/container/deployment/dataflow)
- `ARC-*-DEVO-*.md` — DevOps strategy (CI/CD, environments, observability)
- `ARC-*-SECD-*.md` — Secure by Design assessment
- `ARC-*-PIA-*.md` — PIA (privacy risks and mitigations)
- `ARC-*-SNOW-*.md` — Service management design (operational readiness)

**OPTIONAL** (read if available, skip silently if missing):
- `ARC-*-TCOP-*.md` — Digital Experience Policy / DSS technology governance review
- `ARC-*-AIGA-*.md` / `ARC-*-AITS-*.md` — AI governance (if in scope)
- `ARC-*-RSCH-*.md` (and provider research artefacts) — research and market scanning

### Step 4: Build the DSS Evidence Model

For each DSS criterion:

- Summarise what the criterion means in this project context.
- Map evidence to ArcKit artefacts (by file and section references).
- Identify gaps.
- Provide a readiness rating (🟢 Ready / 🟡 Partial / 🔴 Not Ready).

Use STAGE to tune expectations:

- `discovery`: intent, users, inclusion risks, service ecosystem, early trust and harm analysis.
- `alpha`: prototypes, early service integration approach, early monitoring approach, security/privacy-by-design.
- `beta`: implementation evidence, live-like monitoring, operational readiness, incident/change readiness.
- `live`: operating model evidence, measurement cadence, continuous improvement loop, currency and relevance.

### Step 5: Produce the Report

Use the template structure and populate:

- Executive summary and readiness score (out of 10 criteria)
- A full criterion-by-criterion section (1-10)
- Evidence inventory table (criterion → artefacts → RAG → critical gaps)
- Action plan (Critical/High/Medium)
- Assurance review session guidance (agenda, presenters, artefacts to bring)

### Step 6: Write Output

Write:

- `projects/{project-dir}/ARC-{PROJECT_ID}-SVCASS-v${VERSION}.md`

Show only a concise summary (overall RAG, readiness score, top gaps, next steps). Do not print the whole report.

## Related Commands

- `/arckit.tcop` — Digital Experience Policy / technology governance review
- `/arckit.secure` — Secure by Design assessment (AU policy baseline)
- `/arckit.pia` — PIA (OAIC-aligned)
- `/arckit.traceability` — Traceability matrix
- `/arckit.analyze` — Governance quality analysis
