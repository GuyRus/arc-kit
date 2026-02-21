# Privacy Impact Assessment (PIA)

> **Template status**: Beta | **Version**: [VERSION] | **Command**: `/arckit.dpia` (ArcKit uses the `DPIA` document type for backwards compatibility)

A Privacy Impact Assessment (PIA) is a written assessment that identifies how an activity or function might impact the privacy of individuals and sets out recommendations to manage, minimise, or eliminate that impact.

This template follows the OAIC PIA Guide’s 10-step flow:
1. Threshold assessment
2. Plan the PIA
3. Describe the project
4. Consult
5. Map information flows
6. Privacy analysis / compliance check
7. Identify privacy impacts and risks
8. Recommendations
9. Report and sign-off
10. Respond and review

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | {document_id} |
| **Document type** | Privacy Impact Assessment (PIA) |
| **Project** | [PROJECT_NAME] (Project [PROJECT_ID]) |
| **Classification** | [OFFICIAL / OFFICIAL:Sensitive / PROTECTED / SECRET / TOP SECRET] |
| **Status** | [DRAFT / IN_REVIEW / APPROVED / SUPERSEDED / ARCHIVED] |
| **Version** | [VERSION] |
| **Created date** | [YYYY-MM-DD] |
| **Last modified** | [YYYY-MM-DD] |
| **Assessment date** | [YYYY-MM-DD] |
| **Owner** | [OWNER_NAME_AND_ROLE] |
| **Senior Responsible Owner (SRO)** | [NAME] |
| **Privacy Officer** | [NAME] |
| **Security lead** | [NAME] |
| **Records / information management** | [NAME] |
| **System owner / product owner** | [NAME] |
| **Next review date** | [YYYY-MM-DD] |
| **Review triggers** | [Material change / New data flow / New vendor / New purpose / Incident / Policy change] |
| **PIA register entry (if applicable)** | [REGISTER_ID / LINK] |
| **Personal information holdings register updated (if applicable)** | [YES/NO] |

## Revision History

| Version | Date | Author | Changes | Approved by | Approval date |
|---------|------|--------|---------|-------------|---------------|
| [VERSION] | [DATE] | ArcKit AI | Initial creation from `/arckit.dpia` | [PENDING] | [PENDING] |

## Executive Summary

**What is being assessed?**
- **Activity / function**: [ACTIVITY_NAME]
- **Scope**: [FULL SYSTEM / FEATURE / DATA FLOW]
- **Assessment approach**: [Comprehensive PIA / Targeted PIA]

**Summary of personal information handling**
- **Individuals affected**: [DATA SUBJECT GROUPS]
- **Personal information**: [SUMMARY OF CATEGORIES]
- **Sensitive information (Privacy Act s 6(1))**: [YES/NO] — [CATEGORIES]
- **High-impact decisions**: [YES/NO] — [ELIGIBILITY / ENTITLEMENTS / SANCTIONS / ENFORCEMENT / OTHER]
- **Outsourcing / vendors**: [YES/NO] — [VENDORS]
- **Overseas disclosure / access** (APP 8): [YES/NO] — [COUNTRIES / SUPPORT LOCATIONS]

**Overall privacy risk**
- **Residual risk rating**: [LOW / MEDIUM / HIGH]
- **Key privacy risks**:
  - PIA-001: [RISK]
  - PIA-002: [RISK]
  - PIA-003: [RISK]

**Key recommendations**
- [Recommendation 1]
- [Recommendation 2]
- [Recommendation 3]

**Decision**
- **Proceed**: [YES/NO/YES WITH CONDITIONS]
- **Conditions / dependencies**: [SUMMARY]

---

## 1. Threshold Assessment (OAIC Step 1)

Record why a PIA is needed and how detailed it should be.

| Indicator | YES/NO | Evidence |
|----------|--------|----------|
| Personal information involved | [YES/NO] | [Data model entities/attributes] |
| Sensitive information involved (Privacy Act s 6(1)) | [YES/NO] | [Data model / classification] |
| Large volume, aggregation, or new central dataset | [YES/NO] | [Scale, duration, retention] |
| New/novel technology | [YES/NO] | [AI/ML, biometrics, monitoring, etc.] |
| Outsourcing / external providers (incl. overseas support) | [YES/NO] | [Vendor model, hosting, support] |
| Cross-entity sharing, matching, or combining datasets | [YES/NO] | [Integrations, data matching] |
| Compulsory collection / power imbalance | [YES/NO] | [Gov-citizen, employer-employee, etc.] |
| Potential adverse outcomes for individuals | [YES/NO] | [Decision impacts / harms] |

**Threshold outcome**
- **PIA decision**: [Proceed with comprehensive PIA / Proceed with targeted PIA / PIA deferred]
- **Rationale**: [Explain]
- **Decision maker**: [NAME, ROLE]
- **Decision date**: [YYYY-MM-DD]

**If this is an Australian Government agency**
- Note: The Privacy Act provides that the Commissioner may direct an agency to provide a PIA where a proposed activity or change might have a significant impact on privacy (Privacy Act 1988 s 33D).

---

## 2. Plan the PIA (OAIC Step 2)

**PIA objectives**
- [What decisions this PIA will inform]

**Assessment team and roles**

| Role | Name | Responsibilities |
|------|------|------------------|
| PIA lead | [NAME] | Coordinate inputs; maintain evidence; manage approvals |
| Privacy Officer | [NAME] | APP interpretation; privacy governance; register updates |
| Security lead | [NAME] | APP 11 security; threat scenarios; control selection |
| Records / IM | [NAME] | Retention, disposal, records authority constraints |
| Legal / policy | [NAME] | Legislative authority; legal basis for collection/disclosure |
| Service / product owner | [NAME] | Purpose, user journeys, operational decisions |
| Vendor manager | [NAME] | Contract terms; assurance; subcontractors |

**Inputs and evidence**
- Data model and personal information inventory (`ARC-*-DATA-*.md`)
- Requirements / business rules (`ARC-*-REQ-*.md`)
- Stakeholders and affected individuals (`ARC-*-STKE-*.md`)
- Security assessment (`ARC-*-SECD-*.md`) and risk register (`ARC-*-RISK-*.md`)
- Vendor due diligence, DPIAs/PIAs, contracts, and hosting/support locations

**Deliverables**
- PIA report (this document)
- Action plan and owners
- Updates to privacy notice(s) / collection notice(s) (APP 5) where required
- (If applicable) AI impact assessment artefact(s) and AI transparency statement

**Milestones**

| Milestone | Date | Notes |
|----------|------|------|
| Draft completed | [DATE] | |
| Stakeholder consultation completed | [DATE] | |
| Security and records review completed | [DATE] | |
| Governance sign-off | [DATE] | |
| Post-implementation review | [DATE] | |

---

## 3. Describe the Project / Activity (OAIC Step 3)

### 3.1 Overview
- **Problem statement**: [What is being solved]
- **Proposed solution**: [System/process summary]
- **In/out of scope**: [Boundaries]

### 3.2 Individuals and context
- **Individuals affected**: [Groups]
- **Power imbalance**: [YES/NO] — [Details]
- **Vulnerable groups**: [YES/NO] — [Details]

### 3.3 Legal and policy context
Describe the authority and constraints relevant to this activity:
- **Authorising legislation / policy** (if applicable): [CITATIONS]
- **Contractual constraints**: [CITATIONS]
- **Records and retention constraints**: [Records authorities / Archives Act / PSPF obligations]

If any legal authority is unclear, record it as a decision point and seek legal advice.

---

## 4. Consultation (OAIC Step 4)

PIAs should consider consultation proportionate to the privacy risks.

### 4.1 Internal consultation

| Stakeholder | Role | Input needed | Date | Outcome |
|------------|------|--------------|------|---------|
| [NAME] | Privacy | APP mapping, notices, governance | [DATE] | [NOTES] |
| [NAME] | Security | Threats, controls, monitoring | [DATE] | [NOTES] |
| [NAME] | Records / IM | Retention and disposal constraints | [DATE] | [NOTES] |
| [NAME] | Service owner | Business purpose and user journeys | [DATE] | [NOTES] |
| [NAME] | Legal | Authority and disclosure basis | [DATE] | [NOTES] |

### 4.2 External consultation (where appropriate)
- **Method**: [Surveys / Interviews / Workshops / Not practicable]
- **Participant groups**: [Groups]
- **Key findings**: [Findings]
- **How findings changed the design**: [Changes]

If consultation is not practicable, record why (for example, security-sensitive activity) and what alternative checks were performed (e.g., representative panels, research, community expectations).

---

## 5. Information Flows and Lifecycle Mapping (OAIC Step 5)

### 5.1 End-to-end lifecycle
Describe how personal information moves through the system:
- Collection
- Storage
- Use
- Disclosure
- Retention
- Disposal / de-identification

Include a data flow diagram if available.

### 5.2 Personal information inventory summary
Summarise from the data model and highlight any gaps.

| Data set / entity | Personal information | Sensitive information | Source | Primary purpose | Key disclosures | Retention / disposal |
|------------------|----------------------|----------------------|--------|-----------------|----------------|----------------------|
| [ENTITY] | [FIELDS] | [YES/NO + categories] | [SOURCE] | [PURPOSE] | [RECIPIENTS] | [RETENTION] |

### 5.3 Disclosures and sharing

| Recipient | Disclosure type | Personal information disclosed | Purpose | Contract / assurance | Overseas? |
|----------|------------------|-------------------------------|---------|----------------------|----------|
| [Vendor/Agency] | [Use/Disclosure] | [Fields] | [Purpose] | [Contract clauses / audit] | [YES/NO] |

### 5.4 Overseas disclosure / access (APP 8)
- **Overseas recipients**: [List]
- **Countries / regions**: [List]
- **Why overseas access occurs**: [Hosting, support, monitoring, subcontractors]
- **Control approach**: [Contractual restrictions, technical controls, assurance programme]

---

## 6. Privacy Analysis and Compliance Check (OAIC Step 6)

Assess compliance with the Privacy Act 1988 and Australian Privacy Principles (APPs). Mark each item as:
- **Met**: evidence exists and is implemented
- **Gap**: must be implemented
- **Not applicable**: with rationale

### 6.1 APP compliance matrix

| Obligation | Met/Gap/N/A | Evidence | Gap / action |
|-----------|-------------|----------|--------------|
| **APP 1** Open and transparent management of personal information | [ ] | [Privacy management plan, governance, PIA register] | [Actions] |
| **APP 2** Anonymity and pseudonymity (where practicable) | [ ] | [User journey; alternative channels] | [Actions] |
| **APP 3** Collection of solicited personal information (reasonably necessary; lawful and fair) | [ ] | [Collection points; purpose mapping] | [Actions] |
| **APP 4** Unsolicited personal information (handling and destruction) | [ ] | [Inbound channels; triage process] | [Actions] |
| **APP 5** Notification of collection (collection notices; transparency) | [ ] | [Notices; privacy policy updates; chatbot labelling] | [Actions] |
| **APP 6** Use or disclosure (primary purpose; consent; reasonable expectations; sensitive info constraints) | [ ] | [Purpose register; disclosure controls] | [Actions] |
| **APP 7** Direct marketing (if applicable) | [ ] | [Opt-out; preference centre] | [Actions] |
| **APP 8** Cross-border disclosure (reasonable steps; accountability considerations) | [ ] | [Due diligence; contracts; assurance; s 16C implications] | [Actions] |
| **APP 9** Adoption, use or disclosure of government related identifiers (if applicable) | [ ] | [Identifier design; restrictions] | [Actions] |
| **APP 10** Quality of personal information (accuracy, completeness, up-to-date) | [ ] | [Validation; monitoring; human review; AI hallucination controls] | [Actions] |
| **APP 11** Security of personal information (access control; monitoring; cyber resilience) | [ ] | [Security design; ISM/PSPF alignment; incident response] | [Actions] |
| **APP 11.3** Destruction or de-identification when no longer needed (subject to records constraints) | [ ] | [Retention schedule; disposal workflow; records authority check] | [Actions] |
| **APP 12** Access to personal information | [ ] | [Access pathway; service support; identity verification] | [Actions] |
| **APP 13** Correction of personal information | [ ] | [Correction workflow; downstream propagation] | [Actions] |

### 6.2 Notifiable Data Breaches (NDB) readiness
Confirm the project can detect, assess, and respond to suspected eligible data breaches.

- **Suspected eligible data breach assessment window**: [Process supports assessment within 30 days]
- **Notification**: [Process supports notification to OAIC and affected individuals as soon as practicable if an eligible data breach occurs]
- **Playbooks**: [Links]
- **Logging and evidence**: [What logs exist]

### 6.3 Contracting and vendors (privacy-by-design controls)
Summarise how vendors are controlled, including:
- Contractual restrictions on use/disclosure and subcontracting
- Controls for overseas access and support
- Security obligations and assurance activities
- Data return/destruction at contract end

---

## 7. Privacy Impacts and Risk Assessment (OAIC Step 7)

Assess privacy harms from the perspective of individuals (not only organisational risk).

### 7.1 Risk scale
- **Likelihood**: Remote / Possible / Probable
- **Consequence (impact on individuals)**: Minimal / Significant / Severe
- **Overall risk**: Low / Medium / High

### 7.2 Risk register (PIA)

| Risk ID | Scenario | Individuals affected | APPs / obligations | Likelihood | Consequence | Inherent risk | Existing controls | Treatment / mitigation | Residual risk | Owner | Due |
|--------|----------|----------------------|-------------------|------------|-------------|--------------|------------------|------------------------|--------------|-------|-----|
| PIA-001 | [Describe] | [Groups] | [APP 11, APP 8, NDB] | [ ] | [ ] | [ ] | [Controls] | [Actions] | [ ] | [ ] | [ ] |

Include risks such as:
- Unauthorised access / disclosure (security failure)
- Unintended secondary use (purpose creep)
- Lack of transparency / misleading notices
- Excessive collection or retention
- Cross-border disclosure without adequate controls
- Inaccurate or inferred personal information (including AI hallucinations) leading to harm
- Inability to access/correct information in time
- Discrimination or unfair outcomes from decision support / automation

---

## 8. Recommendations and Action Plan (OAIC Step 8)

Translate mitigations into clear actions.

| Recommendation ID | Recommendation | Priority | Owner | Due date | Status | Evidence of completion |
|------------------|----------------|----------|-------|----------|--------|------------------------|
| REC-001 | [Do X] | [High/Med/Low] | [Name] | [Date] | [Open/In progress/Done] | [Link] |

**Residual risk acceptance**
- If any residual risk remains **High**, document escalation to privacy/legal governance and the decision (including rationale and conditions).

---

## 9. Report, Sign-off, and Handling (OAIC Step 9)

### 9.1 Approval

| Role | Name | Signature | Date |
|------|------|-----------|------|
| Service / product owner | [NAME] |  |  |
| Privacy Officer | [NAME] |  |  |
| Security lead | [NAME] |  |  |
| Records / IM | [NAME] |  |  |
| SRO | [NAME] |  |  |

### 9.2 Distribution and storage
- **Storage location**: [Repository/path]
- **Who can access**: [Groups]
- **External release**: [If a public summary will be published, describe what is redacted]

---

## 10. Respond and Review (OAIC Step 10)

### 10.1 Implementation tracking
- **Where actions are tracked**: [Backlog / risk register / assurance tracker]
- **How completion is verified**: [Evidence types]

### 10.2 Review triggers
Update the PIA when any of the following occurs:
- Material change in scope, purposes, or information flows
- New vendor, new overseas access pattern, or new subcontractor
- Changes to notices, collection channels, or decision logic
- Security incident or suspected eligible data breach
- Relevant OAIC guidance updates or policy changes

### 10.3 Register updates (for agencies and mature privacy governance)
If applicable, record:
- PIA register entry created/updated
- Personal information holdings register updated

For Australian Government agencies, the Privacy (Australian Government Agencies – Governance) APP Code 2017 requires a Privacy Officer to maintain a record of the entity’s personal information holdings and a register of privacy impact assessments.

---

## Appendix A: Detailed Information Flows

Provide detailed flow mapping (system-to-system, API endpoints, batch transfers, manual processes):
- [Flow 1]
- [Flow 2]

## Appendix B: Cross-Border Disclosure Assessment (APP 8)

| Overseas recipient | Country | What is disclosed | Purpose | Reasonable steps (contracts, assurance, technical) | Exception relied upon (if any) |
|-------------------|---------|------------------|---------|---------------------------------------------------|-------------------------------|
| [Recipient] | [Country] | [Fields] | [Purpose] | [Describe] | [APP 8.2? / None] |

## Appendix C: Notifiable Data Breaches (NDB) Checklist

| Item | Yes/No | Notes |
|------|--------|------|
| Incident detection and escalation path exists | [ ] | [Links] |
| Ability to rapidly identify affected individuals and data types | [ ] | [How] |
| Ability to assess serious harm likelihood within 30 days | [ ] | [Process] |
| Templates for notifying OAIC and individuals | [ ] | [Links] |
| Evidence preservation and logging | [ ] | [Logs] |

## Appendix D: AI-Specific Addendum (if applicable)

Complete this section if the project uses AI/ML, deploys decision support, or inputs personal information into generative AI tools.

**AI policy and assurance (Australian Government)**
- **AI use case in scope of DTA AI policy**: [YES/NO/UNKNOWN]
- **AI impact assessment completed**: [YES/NO] — [Link]
- Note: DTA requires agencies to implement mandatory AI impact assessments for in-scope use cases by 15 December 2026.

**Privacy and AI considerations (OAIC guidance)**
- Avoid entering personal information (especially sensitive information) into publicly available generative AI tools.
- If the system generates or infers personal information, treat outputs as personal information and apply APP obligations (including APP 3 and APP 10).
- Document human oversight, transparency measures, and contestability pathways.

| AI risk | Description | Controls | Residual risk |
|--------|-------------|----------|--------------|
| AI-001 | [Bias/unfairness] | [Controls] | [ ] |
| AI-002 | [Hallucination/inaccuracy] | [Controls] | [ ] |
| AI-003 | [Model inversion / leakage] | [Controls] | [ ] |
