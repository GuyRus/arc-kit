# Data Source Discovery (DataScout): [PROJECT_NAME]

> **Template status**: Alpha | **Version**: [VERSION] | **Command**: `/arckit.datascout`

This document records the discovery and evaluation of external data sources (APIs, datasets, registries, and commercial providers) that may fulfil the project’s data and integration requirements.

It is intended to be usable for both Australian Government and Australian enterprise contexts. Where government-specific governance applies (for example, cross-entity data sharing, data matching/linkage, or security classification constraints), call it out explicitly.

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-[PROJECT_ID]-DSCT-v[VERSION] |
| **Document type** | Data Source Discovery |
| **Project** | [PROJECT_NAME] (Project [PROJECT_ID]) |
| **Classification** | [OFFICIAL / OFFICIAL:Sensitive / PROTECTED / SECRET / TOP SECRET] |
| **Status** | [DRAFT / IN_REVIEW / APPROVED / SUPERSEDED / ARCHIVED] |
| **Version** | [VERSION] |
| **Created date** | [YYYY-MM-DD] |
| **Last modified** | [YYYY-MM-DD] |
| **Owner** | [OWNER_NAME_AND_ROLE] |
| **Reviewed by** | [REVIEWER_NAME] ([YYYY-MM-DD]) or PENDING |
| **Approved by** | [APPROVER_NAME] ([YYYY-MM-DD]) or PENDING |
| **Distribution** | [DISTRIBUTION_LIST] |

## Revision History

| Version | Date | Author | Changes | Approved by | Approval date |
|---------|------|--------|---------|-------------|---------------|
| [VERSION] | [DATE] | ArcKit AI | Initial creation from `/arckit.datascout` | PENDING | PENDING |

---

## Executive Summary

### Data Needs Overview

This report identifies external data sources that may fulfil the data and integration requirements in `ARC-{PROJECT_ID}-REQ-v*.md`.

- **Requirements analysed**: [X] DR-xxx, [Y] INT-xxx, [Z] relevant NFR-xxx
- **Discovery scope**: [Open data / Government APIs / Commercial APIs / Research datasets / Mixed]
- **Data domains covered**: [e.g., identity, business registers, geospatial, payments]

### Discovery Approach (Summary)

1. Extract data needs and constraints from requirements (fields, freshness, residency, classification, budget).
2. Search Australian Government catalogues first:
   - `api.gov.au`
   - `data.gov.au`
3. Expand to authoritative custodians (sector agencies/regulators) and commercial providers if open data is insufficient.
4. Evaluate candidates with weighted scoring, produce a ranked shortlist, and record gaps and decision points.

### Key Findings

- [Finding 1]
- [Finding 2]
- [Finding 3]

### Data Source Summary

| Source type | Count | Typical cost range | Notes |
|------------|-------|--------------------|------|
| Australian Government open data / APIs | [N] | Free / cost-recovery / varies | Evidence links recorded per source |
| State/territory open data / APIs | [N] | Free / varies | Only where relevant |
| Commercial APIs / data products | [N] | $[low]-$[high]/year | Contract and assurance needed |
| Research / open datasets | [N] | Free | Ensure licence terms fit intended use |
| **Total** | [N] |  |  |

### Top Recommended Sources (Shortlist)

| Rank | Source | Type | Coverage (DR/INT) | Key constraints | Overall score |
|------|--------|------|-------------------|----------------|--------------|
| 1 | [Source name] | [API/Dataset] | [DR-xxx, INT-xxx] | [Residency/licence/cost] | [0-100] |
| 2 | [Source name] | [API/Dataset] | [DR-xxx, INT-xxx] | [Constraints] | [0-100] |
| 3 | [Source name] | [API/Dataset] | [DR-xxx, INT-xxx] | [Constraints] | [0-100] |

### Requirements Coverage

- **Covered**: [N]/[M] ([%])
- **Partially covered**: [N] (coverage or quality constraints)
- **Gaps**: [N] (no suitable source)

### Privacy, Security, and Data-Sharing Flags

| Flag | YES/NO/UNKNOWN | Why it matters | Action |
|------|-----------------|---------------|--------|
| Personal information involved | [ ] | May trigger Privacy Act/APP obligations | Run `/arckit.pia` |
| Sensitive information involved (Privacy Act s 6(1)) | [ ] | Higher privacy risk | Run `/arckit.pia` + governance escalation |
| Cross-border disclosure/access likely (APP 8) | [ ] | Cross-border assessment required | Document in PIA and supplier terms |
| Data matching/linkage proposed | [ ] | Requires governance scrutiny | Document controls and approvals |
| Classification constraints apply (PSPF/ISM) | [ ] | Impacts hosting, access, handling | Confirm architecture alignment |

---

## 1. Inputs and Constraints

### 1.1 Inputs

| Input | Status | Notes |
|------|--------|------|
| Requirements (`ARC-*-REQ-*.md`) | MANDATORY | Extract DR/INT/NFR constraints |
| Data model (`ARC-*-DATA-*.md`) | RECOMMENDED | Map sources to entities/attributes and flows |
| Stakeholders (`ARC-*-STKE-*.md`) | RECOMMENDED | Identify affected groups, quality expectations |
| Architecture principles (`ARC-000-PRIN-*.md`) | RECOMMENDED | Apply sourcing, privacy, and security constraints |
| Existing catalogues / contracts | OPTIONAL | Reuse known sources; avoid duplicative discovery |

### 1.2 Constraints to Apply

| Constraint | Value | Source |
|-----------|-------|--------|
| Data residency | [AU-only / Any / restricted] | [NFR/policy] |
| Freshness / update frequency | [Realtime/daily/weekly/monthly] | [DR/NFR] |
| Latency (for API use) | [e.g., p95 < 200ms] | [NFR] |
| Budget | [$ / year] | [Business case] |
| Allowed licences | [e.g., CC BY 4.0 / bespoke] | [Policy] |
| Security classification | [OFFICIAL / OFFICIAL:Sensitive / ...] | [PSPF/ISM] |
| Downstream disclosure | [Internal-only / external] | [Architecture] |
| Data minimisation expectation | [Yes/No] | [Privacy principles] |

### 1.3 Assumptions and Unknowns

| Item | Assumption / unknown | Impact | Owner | Due |
|------|-----------------------|--------|-------|-----|
| [A-001] | [Unknown licence terms] | Blocks selection | [Name] | [Date] |

---

## 2. Data Needs (Extracted From Requirements)

Summarise external data needs and the minimum viable fields.

| Need ID | Requirement IDs | Data needed | Minimum fields | Freshness | Volume | Notes |
|--------|------------------|------------|----------------|----------|--------|------|
| NEED-001 | [DR-xxx, INT-xxx] | [Description] | [Fields] | [SLA] | [Volume] | [Notes] |

### 2.1 Scenario Matrix (Prompt Seeds)

Use these scenario prompts to drive targeted discovery and keep results decision-ready.

| Scenario | Prompt seed | Focus |
|---------|-------------|-------|
| Open data first | "Discover Australian Government open data and APIs for <need>" | api.gov.au, data.gov.au, custodians |
| Commercial alternatives | "Find commercial APIs for <capability> in Australia" | pricing, SLAs, coverage |
| Gap analysis | "Identify which requirements have no external source" | fallbacks and options |
| Data model enrichment | "Map sources to entities and attributes" | schema impact and sync |
| Privacy flags | "Does this source contain personal information?" | trigger PIA and governance |

---

## 3. Discovery Approach and Sources Checked

### 3.1 Mandatory starting points (AU)

Record what was searched and when:

| Source | Accessed on | Notes |
|--------|-------------|------|
| api.gov.au | [YYYY-MM-DD] | API directory results logged |
| data.gov.au | [YYYY-MM-DD] | Dataset catalogue results logged |

### 3.2 Custodians and sector sources (as applicable)

Record only what was relevant:

| Domain | Custodian / portal | Accessed on | Notes |
|-------|---------------------|-------------|------|
| Statistics | ABS | [DATE] | |
| Weather/environment | BoM / environment portals | [DATE] | |
| Energy | AEMO / AER | [DATE] | |
| Geospatial | Geoscience Australia / state spatial portals | [DATE] | |
| Business registers | ABR / ASIC / ACNC | [DATE] | |

### 3.3 Commercial and other sources

| Provider | Accessed on | Notes |
|----------|-------------|------|
| [Provider] | [DATE] | |

---

## 4. Evaluation Framework

### 4.1 Scoring weights

| Criterion | Weight | What it measures |
|-----------|--------|------------------|
| Requirements fit | 25% | Field coverage, scope, freshness |
| Data quality | 20% | Accuracy, completeness, timeliness, representativeness |
| Licence and cost | 15% | Licence permissions, attribution, sustainability |
| API/data delivery quality | 15% | Docs, stability, versioning, auth, formats |
| Privacy and governance | 15% | Privacy Act/APP fit, sharing authority, matching concerns |
| Reliability and support | 10% | Uptime/SLA, vendor maturity, support |

### 4.2 Evaluation criteria explained (what to look for)

- **Requirements fit**: minimum fields present; geographic/temporal coverage; update frequency.
- **Data quality**: published methodology; known gaps; validation routines; provenance.
- **Licence and cost**: permitted uses; downstream redistribution; attribution; change-in-terms risk.
- **Delivery quality**: API stability, pagination, limits, auth; bulk formats; schemas.
- **Privacy and governance**: whether data includes personal information; cross-border data flow; data matching/linkage concerns.
- **Reliability and support**: SLAs, incident comms, deprecation policies.

### 4.3 Minimum due diligence checklist

| Check | Pass/Fail/NA | Evidence |
|------|--------------|----------|
| Licence/terms permit intended use (incl. downstream disclosure) | [ ] | [Link/quote] |
| Data custodian/owner identified | [ ] | [Owner] |
| Personal information present? If YES, PIA required | [ ] | [Assessment] |
| Cross-border access/disclosure? If YES, APP 8 assessment required | [ ] | [Assessment] |
| Data matching/linkage? If YES, governance required | [ ] | [Assessment] |
| Quality indicators available (metadata, lineage, update logs) | [ ] | [Evidence] |
| Change management/versioning documented | [ ] | [Evidence] |

---

## 5. Candidate Sources (Evaluation Cards)

Create one evaluation card per candidate. Keep claims evidence-based and link to primary sources.

### 5.1 [SOURCE NAME]

**Overview**
- **Provider/custodian**: [Name]
- **Type**: [API / Dataset / Registry / Feed]
- **Access method**: [REST / bulk download / other]
- **URL(s)**: [Link]
- **Auth model**: [API key/OAuth/mTLS/None]
- **Rate limits**: [If known]
- **Update frequency**: [e.g., daily]

**Coverage**
- **Mapped requirements**: [DR-xxx, INT-xxx]
- **Field coverage**: [List]
- **Geographic/temporal scope**: [Scope]

**Quality and risk notes**
- **Known data quality characteristics**: [Notes]
- **Representativeness/bias considerations (if used for analytics/AI)**: [Notes]

**Licence and cost**
- **Licence/terms**: [e.g., CC BY 4.0 / bespoke / unknown]
- **Attribution requirements**: [Yes/no]
- **Cost model**: [Free / subscription / per-call]

**Privacy and governance**
- **Personal information present**: [YES/NO/UNKNOWN]
- **Sensitive information present**: [YES/NO/UNKNOWN]
- **Cross-border disclosure/access**: [YES/NO/UNKNOWN]
- **Data matching/linkage risk**: [Notes]
- **PIA required**: [YES/NO]

**Security and operations**
- **Classification**: [OFFICIAL / OFFICIAL:Sensitive / ...]
- **Storage/handling constraints**: [Notes]
- **Reliability/SLA**: [If known]

**Integration notes**
- **Integration pattern**: [Batch ETL / streaming / API sync]
- **Data model impact**: [New entities/attributes]

**Score**

| Criterion | Score (0-5) | Notes |
|----------|-------------|------|
| Requirements fit | [ ] | |
| Data quality | [ ] | |
| Licence and cost | [ ] | |
| API/data delivery quality | [ ] | |
| Privacy and governance | [ ] | |
| Reliability and support | [ ] | |

**Weighted total**: [0-100]

---

## 6. Comparison Matrices

Provide one comparison table per need/category.

| Source | Fit | Quality | Licence/Cost | Delivery | Privacy/Gov | Reliability | Total |
|--------|-----|---------|--------------|----------|------------|------------|-------|
| [A] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |
| [B] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |

---

## 7. Gap Analysis

| Requirement / Need | Gap | Impact | Options | Recommendation |
|-------------------|-----|--------|--------|----------------|
| [DR-xxx] | [No suitable source] | [Impact] | [Collect internally / negotiate sharing / proxy] | [Recommendation] |

---

## 8. Data Utility Analysis (Beyond Primary Requirements)

For each recommended source, capture additional value (and new risks):

| Source | Primary use | Secondary uses | New risks introduced |
|--------|-------------|----------------|----------------------|
| [Source] | [Use] | [Use] | [Risks] |

---

## 9. Data Model and Architecture Impact

### 9.1 New/changed entities and attributes

| Source | Entity | Attributes | Cardinality | Notes |
|--------|--------|------------|-------------|------|
| [Source] | [Entity] | [Attributes] | [1..*] | [Notes] |

### 9.2 Integration pattern recommendation

| Source | Pattern | Frequency | Idempotency key | Error handling | Notes |
|--------|---------|-----------|------------------|---------------|------|
| [Source] | [Batch/API/Stream] | [Freq] | [Key] | [Approach] | [Notes] |

---

## 10. Privacy, Security, and Governance Considerations

### 10.1 Privacy impacts

If any candidate source includes personal information or is used in a way that creates personal information about individuals, record:
- why the use is necessary and proportionate
- how transparency/notice will be handled
- whether a PIA is required (`/arckit.pia`)

### 10.2 Cross-border access/disclosure (APP 8)

If supplier hosting/support involves overseas recipients, record it and ensure it is addressed in the PIA and procurement artefacts.

### 10.3 Data sharing and data matching/linkage

If the proposal involves sharing or matching/linkage:
- document governance approvals required
- describe controls to reduce incorrect matching and adverse impacts
- ensure the project’s risk register reflects these risks

### 10.4 Security classification and handling

Confirm that classification and handling constraints are compatible with the proposed architecture (hosting, access control, logging).

---

## 11. Decision Log and Next Steps

### 11.1 Decisions to capture as ADRs

| Decision | ADR required? | Notes |
|---------|----------------|------|
| Select primary source for NEED-001 | [YES/NO] | [Notes] |

### 11.2 Next steps

1. Update the data model (`/arckit.data-model`) with selected sources.
2. Record sourcing decisions as ADRs (`/arckit.adr`).
3. If personal information is involved, complete/update the PIA (`/arckit.pia`) and address APP 8 if relevant.
4. Update risks in the risk register (`/arckit.risk`).
5. Create or update data flow diagrams (`/arckit.diagram`).
