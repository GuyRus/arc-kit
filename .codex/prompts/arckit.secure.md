---
description: "Generate a Secure by Design assessment for Australian Government projects (AU civilian, PSPF/ISM/Essential Eight aligned)"
---

# Australian Government Secure by Design Assessment (`/arckit.secure`)

You are helping to produce a **Secure by Design assessment** for an Australian Government technology project (civilian / non-Defence).

The output must preserve useful, generic Secure by Design structure (executive summary, evidence inventory, findings, actions, traceability) while aligning the content to Australian Government expectations first.

## User Input

```text
$ARGUMENTS
```

## Australian Context (What This Must Align To)

This assessment should be anchored in the following Australian Government-aligned expectations (tailored to the system and agency):

- **ASD Essential Eight** maturity expectations (current vs target)
- **Agency security policy** and mandatory control sets aligned to the **PSPF** and **ISM** (do not invent control IDs; describe control intent and evidence)
- **Cloud security and assurance** approach (shared responsibility, logging, encryption, IAM guardrails) and **IRAP readiness where required**
- **Privacy Act 1988 (APPs)** obligations (where personal information is handled) and readiness for the **Notifiable Data Breaches (NDB) scheme**

If the user’s artefacts indicate AI/ML components, add AI-relevant security considerations (e.g., prompt injection, model/data supply chain, data leakage) but keep them proportionate and evidence-based.

## Your Task

Generate a comprehensive Secure by Design assessment document by:

### 1. Load The Template (User Override Supported)

- **First**, check if `.arckit/templates/secure-by-design-template.md` exists
- **If found**: read it and use it (user override takes precedence)
- **If not found**: read `.arckit/templates/secure-by-design-template.md` (default)

> **Note**: Read `.arckit/VERSION` and update the template metadata version when generating.
> **Tip**: Users can customise templates with `/arckit.customize secure`.

### 2. Understand Project Context (Ask If Missing)

Extract or ask for:

- organisation/agency context (civilian; any agency-specific policy constraints)
- delivery stage (Discovery / Alpha / Beta / Live, or equivalent)
- system type and exposure (public-facing, staff-only, API, data platform)
- information/data classification (use AU style, e.g. `OFFICIAL:Sensitive`)
- hosting model (cloud/on-prem/hybrid) and key vendors
- whether personal information is processed (privacy scope)
- whether IRAP is expected/required in this context (if unclear, ask and record assumption)

### 3. Read Available ArcKit Artefacts

Scan the project directory and read what exists.

**MANDATORY** (warn if missing):

- `ARC-*-REQ-*.md` in `projects/{project}/` — Requirements
  - Extract: NFR-SEC, NFR-A, NFR-R, identity, logging, incident response, data handling constraints
  - If missing: warn user to run `/arckit.requirements` first
- `ARC-000-PRIN-*.md` in `projects/000-global/` — Principles
  - Extract: mandatory guardrails, approved platforms, security expectations
  - If missing: warn user to run `/arckit.principles` first

**RECOMMENDED** (read if available; note if missing):

- `ARC-*-RISK-*.md` — Risk register (security/privacy risks, treatments, risk appetite)
- `ARC-*-PIA-*.md` — Privacy impact assessment (APP risks, mitigations, data sharing constraints)
- `ARC-*-DIAG-*.md` — Architecture diagrams (trust boundaries, data flows, deployment topology)
- `ADR-*.md` — ADRs (security-significant decisions and accepted trade-offs)

**OPTIONAL** (read if available; skip silently if missing):

- `ARC-*-TCOP-*.md` — DX Policy / DSS review (security-related findings)
- `ARC-*-AIGA-*.md` — AU AI governance assessment (AI-specific risks and controls)
- `ARC-*-AITS-*.md` — AI transparency statement (AI usage context and constraints)

### 4. Read External Evidence (If Provided)

Look in `projects/{project}/external/` for PDFs, docs, and images (pen test reports, vulnerability scans, audit reports, threat models).

If none are found, prompt (non-blocking):

“If you have existing security assessments, pen test reports, or threat models, place them in `projects/{project}/external/` and re-run. Otherwise I’ll proceed based on ArcKit artefacts.”

### 5. Perform The Assessment (AU-Aligned Control Areas)

Assess the system across these control areas using the template, and for each area provide:

- status: ✅ Achieved / ⚠️ Partially Achieved / ❌ Not Achieved / N/A
- evidence (links to artefacts, decisions, diagrams)
- findings (what’s missing, what’s risky, what’s strong)
- actions (clear remediation steps with owners and target dates)

**Control areas** (minimum):

- Governance, risk, and assurance (risk ownership, assurance gates, supplier assurance)
- Identity, access, and privilege management (MFA, PAM, least privilege, account lifecycle)
- Data protection and privacy (classification/handling, encryption and keys, retention/disposal, APP obligations, NDB readiness)
- Platform, network, and endpoint security (hardening, patching, segmentation, environment separation)
- Secure engineering and supply chain (secure SDLC, CI/CD checks, dependency risk, SBOM/provenance where appropriate)
- Logging, monitoring, and detection (coverage, retention, alerting, vulnerability management cadence)
- Incident response and resilience (playbooks, backups, recovery objectives, exercises)
- Cloud security and shared responsibility (if applicable), including IRAP readiness where required

**Recommended deep dives** (include when applicable; expected for Beta/Live for internet-facing or sensitive systems):

- vulnerability and patch management (coverage, SLAs, exception process, trend metrics)
- third-party and supply chain risk (supplier access, contractual controls, OSS/dependency controls)
- backup/restore/DR readiness (RTO/RPO, restore tests, ransomware resilience)
- secure SDLC and DevSecOps controls (threat modelling, SAST/DAST/SCA, secrets scanning, IaC scanning, build provenance)

### 6. Essential Eight Maturity Assessment

Include an Essential Eight table (all 8 strategies) with:

- current maturity level (0-3)
- target maturity level (0-3)
- evidence and gaps/actions

Do not claim “certification” levels; treat maturity as an evidence-based assessment.

### 7. Privacy And NDB Readiness (If In Scope)

If personal information is processed:

- summarise key APP areas relevant to the system and what evidence supports compliance
- confirm whether a PIA exists (or recommend one where high privacy risk exists)
- include NDB readiness: detection, triage, “eligible data breach” decision process, notification approach and supplier SLAs

Avoid UK/EU-specific constructs (e.g., “lawful basis”, “ROPA”, “72 hour notification”) unless the project explicitly operates under those regimes.

### 8. Versioning And Output Location

Before generating the document ID, detect whether a previous version exists:

- look for existing `ARC-{PROJECT_ID}-SECD-v*.md` files in the project directory
- if none: `VERSION="1.0"`
- if found: read the latest and decide:
  - **minor** bump (e.g., 1.0 → 1.1): refreshed assessment; same scope
  - **major** bump (e.g., 1.0 → 2.0): scope materially changed; new environments, new assurance boundary, major architecture shift

Save to:

`projects/[project]/ARC-{PROJECT_ID}-SECD-v${VERSION}.md`

### 9. Auto-Populate Document Control Fields (Required)

Generate the Document ID:

```bash
DOC_ID=$(.arckit/scripts/bash/generate-document-id.sh "${PROJECT_ID}" "SECD" "${VERSION}")
```

Populate all document control fields, including classification (AU style, default `OFFICIAL` unless the project context indicates otherwise).
