# Data Source Discovery (DataScout): [PROJECT_NAME]

> **Template status**: Alpha | **Version**: [VERSION] | **Command**: `/arckit.datascout`

This document records the discovery and evaluation of external data sources (APIs, datasets, registries, and commercial providers) that may fulfil the project’s data and integration requirements.

It is written to support Australian Government and Australian enterprise contexts. It includes privacy and data-sharing considerations so decisions are evidence-based and traceable.

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

### Scope
- **Discovery scope**: [Open data / Government APIs / Commercial APIs / Research datasets / Mixed]
- **In-scope requirements**: [List key DR/INT/FR IDs]
- **Out of scope**: [List exclusions]

### Recommendation Snapshot

| Rank | Source | Type | Coverage (DR/INT) | Key constraints | Overall score |
|------|--------|------|-------------------|----------------|--------------|
| 1 | [Source name] | [API/Dataset] | [DR-xxx, INT-xxx] | [Residency/licence/cost] | [0-100] |
| 2 | [Source name] | [API/Dataset] | [DR-xxx, INT-xxx] | [Constraints] | [0-100] |
| 3 | [Source name] | [API/Dataset] | [DR-xxx, INT-xxx] | [Constraints] | [0-100] |

### Coverage
- **Requirements covered**: [N]/[M] ([%])
- **Key gaps**: [Short list]

### Privacy and Data-Sharing Flags
- **Personal information involved**: [YES/NO/UNKNOWN]
- **Sensitive information involved (Privacy Act s 6(1))**: [YES/NO/UNKNOWN]
- **Cross-border disclosure/access likely (APP 8)**: [YES/NO/UNKNOWN]
- **Data matching / linkage involved**: [YES/NO/UNKNOWN]

If any of the above are **YES**, create or update a PIA (`/arckit.pia`) and ensure relevant governance review.

---

## 1. Inputs and Constraints

### 1.1 Inputs

| Input | Status | Notes |
|------|--------|------|
| Requirements (`ARC-*-REQ-*.md`) | MANDATORY | Extract DR/INT/NFR constraints |
| Data model (`ARC-*-DATA-*.md`) | RECOMMENDED | Identify entities/attributes to populate |
| Stakeholders (`ARC-*-STKE-*.md`) | RECOMMENDED | Identify intended users and quality needs |
| Architecture principles (`ARC-000-PRIN-*.md`) | RECOMMENDED | Apply sourcing and compliance constraints |
| Existing catalogues / contracts | OPTIONAL | Reuse known sources where appropriate |

### 1.2 Constraints to Apply

| Constraint | Value | Source |
|-----------|-------|--------|
| Data residency | [AU-only / Any / Restricted by provider] | [NFR / policy] |
| Update frequency | [Realtime/daily/weekly/monthly] | [DR/NFR] |
| Latency | [e.g., p95 < 200ms] | [NFR] |
| Budget | [$/month] | [Business case] |
| Allowed licences | [e.g., CC BY / CC BY-SA / bespoke] | [Policy] |
| Security classification | [OFFICIAL / OFFICIAL:Sensitive / ...] | [PSPF/ISM] |
| Downstream disclosures | [Internal-only / external] | [Architecture] |

---

## 2. Data Needs (Extracted From Requirements)

Create a concise inventory of external data needs.

| Need ID | Requirement IDs | Data needed | Minimum fields | Freshness | Volume | Notes |
|--------|------------------|------------|----------------|----------|--------|------|
| NEED-001 | [DR-xxx, INT-xxx] | [Description] | [Fields] | [SLA] | [Volume] | [Notes] |

---

## 3. Discovery Approach and Sources Checked

### 3.1 Mandatory starting points (AU)
Record what was searched and when:
- `api.gov.au` (Australian Government API directory)
- `data.gov.au` (Australian open data catalogue)

### 3.2 Other common AU sources (as applicable)
Document which of these were relevant and searched:
- Australian Bureau of Statistics (ABS)
- Bureau of Meteorology (BoM)
- Geoscience Australia
- Australian Institute of Health and Welfare (AIHW)
- State/territory open data portals and sector registries

### 3.3 Commercial and other sources
Record commercial providers and industry sources searched:
- [Provider]
- [Provider]

---

## 4. Evaluation Framework

### 4.1 Scoring weights

| Criterion | Weight | What it measures |
|-----------|--------|------------------|
| Requirements fit | 25% | Field coverage, geographic scope, granularity, freshness |
| Data quality | 20% | Accuracy, completeness, timeliness, bias/representativeness |
| Licence and cost | 15% | Licence permissions, attribution, restrictions, sustainability |
| API/data delivery quality | 15% | Documentation, stability, versioning, auth, formats |
| Privacy and governance | 15% | Privacy Act/APP alignment, sharing authority, data matching considerations |
| Reliability and support | 10% | Uptime/SLA, support model, vendor maturity |

### 4.2 Minimum due diligence checklist

| Check | Pass/Fail/NA | Evidence |
|------|--------------|----------|
| Licence/terms permit intended use (including downstream sharing) | [ ] | [Link/quote] |
| Data custodian/owner identified | [ ] | [Owner] |
| Security classification acceptable for storage/handling | [ ] | [Classification] |
| Personal information present? If YES, PIA required | [ ] | [Assessment] |
| Cross-border access/disclosure? If YES, APP 8 assessment required | [ ] | [Assessment] |
| Data matching/linkage? If YES, data matching governance required | [ ] | [Assessment] |
| Quality checks available (metadata, lineage, update logs) | [ ] | [Evidence] |
| Change management/versioning documented | [ ] | [Evidence] |

---

## 5. Candidate Sources (Evaluation Cards)

Create one evaluation card per candidate. Keep the facts evidence-based.

### 5.1 [SOURCE NAME]

**Overview**
- **Provider/custodian**: [Name]
- **Type**: [API / Dataset / Registry / Feed]
- **Access method**: [REST / GraphQL / Bulk download / SFTP / Other]
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
- **Sharing/matching concerns**: [Notes]
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

For each recommended source, capture additional value (and risks):
- Secondary uses (analytics, operations, service improvement)
- Monitoring/observability uses
- AI/ML uses (only if policy and governance permit)

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

## 10. Decision Log and Next Steps

### 10.1 Decisions to capture as ADRs

| Decision | ADR required? | Notes |
|---------|----------------|------|
| Select primary data source for NEED-001 | [YES/NO] | [Notes] |

### 10.2 Next steps

1. Update the data model (`/arckit.data-model`) with selected sources.
2. Record sourcing decisions as ADRs (`/arckit.adr`).
3. If personal information is involved, complete/update the PIA (`/arckit.pia`) and address APP 8 if relevant.
4. Update risks in the risk register (`/arckit.risk`).
5. Create or update data flow diagrams (`/arckit.diagram`).
