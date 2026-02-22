---
description: "Generate a Defence Secure by Design assessment for Australian Defence projects (AU Defence, continuous assurance aligned)"
---

# Defence Secure by Design Assessment (`/arckit.mod-secure`)

You are helping to produce a **Defence Secure by Design assessment** for an Australian Defence context (projects, programmes, capabilities).

The output must preserve useful, generic Secure by Design structure (executive summary, evidence inventory, findings, actions, traceability) while aligning to Australian context first and avoiding UK-specific policy frameworks.

## User Input

```text
$ARGUMENTS
```

## Australian Defence Context (How To Treat Policy)

Defence security policy, assurance pathways, and accreditation artefacts are often **agency-specific and not fully publicly available**.

You must:

- avoid inventing Defence policy names, dates, or mandated processes if not evidenced in the project artefacts
- include explicit `SOURCE_GAP` notes where the organisation-specific baseline is required to complete the assessment
- still produce a useful, actionable Secure by Design assessment using the evidence available (requirements, risks, diagrams, decisions, external reports)

## Your Task

Generate a comprehensive Defence Secure by Design assessment document by:

### 1. Load The Template (User Override Supported)

- **First**, check if `.arckit/templates/mod-secure-by-design-template.md` exists
- **If found**: read it and use it (user override takes precedence)
- **If not found**: read `.arckit/templates/mod-secure-by-design-template.md` (default)

> **Note**: Read `.arckit/VERSION` and update the template metadata version when generating.
> **Tip**: Users can customise templates with `/arckit.customize mod-secure`.

### 2. Understand Project Context (Ask If Missing)

Extract or ask for:

- Defence organisation / delivery context (and any partner/coalition constraints)
- delivery stage (Discovery / Alpha / Beta / Live / Through-life, or equivalent)
- system type and exposure (tactical/enterprise; staff-facing/public-facing; connected/disconnected)
- information/data classification and handling constraints (AU style; include dissemination constraints if provided)
- hosting model (Defence networks, cloud/on-prem/hybrid) and key vendors
- whether personal information is processed (privacy scope)

### 3. Read Available ArcKit Artefacts

**MANDATORY** (warn if missing):

- `ARC-*-REQ-*.md` in `projects/{project}/` — Requirements
  - Extract: NFR-SEC, NFR-A, NFR-R, identity, logging, incident response, data handling constraints
  - If missing: warn user to run `/arckit.requirements` first
- `ARC-000-PRIN-*.md` in `projects/000-global/` — Principles
  - Extract: mandatory guardrails, approved platforms, classification handling requirements
  - If missing: warn user to run `/arckit.principles` first

**RECOMMENDED**:

- `ARC-*-RISK-*.md` — Risk register (security risks, treatments, risk acceptance)
- `ARC-*-SECD-*.md` — Civilian Secure by Design assessment (reuse applicable controls/evidence)
- `ARC-*-PIA-*.md` — Privacy impact assessment (if personal information is in scope)
- `ARC-*-DIAG-*.md` — Diagrams (trust boundaries, data flows, deployment topology)
- `ADR-*.md` — ADRs (security-significant decisions and accepted trade-offs)

### 4. Read External Evidence (If Provided)

Look in `projects/{project}/external/` for PDFs/docs/images such as:

- threat models and security architecture reviews
- vulnerability scans and penetration test reports
- accreditation/security assessment artefacts (where provided)
- supplier attestations and assurance reports (where provided)

Proceed without external evidence if none is available.

### 5. Perform The Assessment (Defence Secure By Design)

Using the template, assess the system and produce:

- an executive summary with a clear readiness call
- a control-area assessment with evidence, findings, and actions
- an explicit list of assumptions and `SOURCE_GAP` items that must be confirmed by Defence policy owners

At minimum, cover:

- governance, risk ownership, and assurance gates (including who can accept residual risk)
- identity, access, and privileged administration (including break-glass and operational access)
- data protection, classification handling, and crypto/key management approach
- secure engineering and supply chain controls (SBOM/provenance where appropriate)
- monitoring, logging, detection, and incident response (including operational constraints)
- resilience and recovery (backup, restore, DR exercises)
- environment separation and secure configuration/patching expectations

### 6. Versioning And Output Location

Detect whether a previous version exists:

- look for existing `ARC-{PROJECT_ID}-SECD-MOD-v*.md`
- if none: `VERSION="1.0"`
- if found: minor vs major bump based on whether scope materially changed

Save to:

`projects/[project]/ARC-{PROJECT_ID}-SECD-MOD-v${VERSION}.md`

### 7. Auto-Populate Document Control Fields (Required)

Generate the Document ID:

```bash
DOC_ID=$(.arckit/scripts/bash/generate-document-id.sh "${PROJECT_ID}" "SECD-MOD" "${VERSION}")
```

Populate all document control fields (including AU-style classification).

