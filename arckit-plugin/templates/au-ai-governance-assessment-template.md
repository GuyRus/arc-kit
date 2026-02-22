# AU AI Governance Assessment

> **Template Status**: Stable | **Version**: [VERSION] | **Command**: `/arckit.ai-playbook`

## Document Control

| Field | Value |
|---|---|
| Document ID | ARC-[PROJECT_ID]-AIGA-v[VERSION] |
| Document Type | AU AI Governance Assessment |
| Project | [PROJECT_NAME] (Project [PROJECT_ID]) |
| Classification | [PUBLIC / OFFICIAL / OFFICIAL:Sensitive / PROTECTED / SECRET / TOP SECRET] |
| Status | [DRAFT / IN_REVIEW / APPROVED / PUBLISHED] |
| Version | [VERSION] |
| Created Date | [YYYY-MM-DD] |
| Last Modified | [YYYY-MM-DD] |
| Review Date | [YYYY-MM-DD] |
| Owner | [OWNER_NAME_AND_ROLE] |
| Accountable Official | [NAME_AND_ROLE] |
| Accountable Use Case Owner | [NAME_AND_ROLE] |

## Policy Baseline (AU Federal)

| Source | Why it is in scope | Accessed (AEDT) |
|---|---|---|
| Policy for the responsible use of AI in government 2.0 | Core mandatory policy obligations | 2026-02-15 |
| Standard for accountability 2.0 | AO/AUCO responsibilities + register minimum fields | 2026-02-15 |
| Standard for AI transparency statements 2.0 | Public transparency statement minimum content | 2026-02-15 |
| Guidance for the AI impact assessment tool | 12-section impact assessment method and risk treatment workflow | 2026-02-15 |
| Australian Government AI technical standard | Technical lifecycle controls and monitoring/decommissioning criteria | 2026-02-15 |
| OAIC AI privacy guidance + PIA guidance | APP-aligned privacy by design and PIA expectations | 2026-02-15 |
| Finance national AI assurance framework | Risk-based assurance expectations and evidence discipline | 2026-02-15 |
| PSPF advisory for generative AI | OFFICIAL information handling conditions for GenAI access | 2026-02-15 |

## Executive Summary

**Use case**: [NAME]

**In-scope determination (Appendix C)**: [IN_SCOPE / OUT_OF_SCOPE]

**Inherent risk**: [Low / Medium / High]  
**Residual risk**: [Low / Medium / High]

**High-risk pathway triggered** (if applicable): [Yes/No]

**Key governance decision**: [Proceed / Proceed with conditions / Do not proceed]

**Top conditions / actions**:

| Priority | Action | Owner | Due date |
|---|---|---|---|
| High | [Action] | [Role] | [YYYY-MM-DD] |
| High | [Action] | [Role] | [YYYY-MM-DD] |

**Key linked artefacts**:

- AI impact assessment (AIIA): `ARC-[PROJECT_ID]-AIIA-v[VERSION].md` (if in-scope)
- AI use case register (AIUR): `ARC-[PROJECT_ID]-AIUR-v[VERSION].md`
- AI governance checklist (AIGC): `ARC-[PROJECT_ID]-AIGC-v[VERSION].md`
- AI transparency statement (AITS): `ARC-[PROJECT_ID]-AITS-v[VERSION].md` (when required/published)

---

## 1. Use Case Profile

- **Use case name**: [NAME]
- **Agency reference**: [IDENTIFIER]
- **Lead agency**: [ENTITY]
- **AI technology type**: [Generative AI / ML / NLP / CV / Hybrid]
- **Domain(s)**: [Service delivery / Compliance and fraud detection / etc.]
- **Usage pattern(s)**: [Decision-making and administrative action / Analytics / etc.]
- **Lifecycle stage**: [Discover / Operate / Retire]

### 1.1 System and AI Boundary (What Is “The AI System” Here?)

- **System boundary**: [What is in scope: model(s), prompts, pipelines, integrations, decision points]
- **Deployment context**: [Internal tool / Public-facing service / Decision support / Operational platform]
- **Primary users**: [Staff / public / partners]
- **Human oversight model**: [Human-in-the-loop / Human-on-the-loop / Human-in-command]
- **Failure mode**: [What happens when AI is unavailable/wrong/unsafe]

### 1.2 AI Component Inventory (Generic, Evidence-Based)

| Component | Type | Purpose | Inputs | Outputs | Human control points | Vendor/Owner | Notes |
|---|---|---|---|---|---|---|---|
| [Component] | [GenAI/ML/NLP/CV/etc.] | [Purpose] | [Inputs] | [Outputs] | [Controls] | [Owner] | [Notes] |

### 1.3 Data Sources and Handling Summary

- **Data sources**: [Systems/datasets]
- **Personal information**: [Yes/No + summary]
- **Sensitive/security-classified information**: [Yes/No + summary]
- **Data minimisation**: [Approach]
- **Retention and disposal**: [Approach]

## 2. In-Scope Determination (Policy Appendix C)

Tick all that apply and add evidence.

- [ ] More than insignificant harm is possible if AI fails or is misused.
- [ ] AI materially influences administrative decisions.
- [ ] Public may directly interact with AI or be significantly impacted without human review.
- [ ] AI uses personal/sensitive/security-classified information.
- [ ] DTA has identified the use case as elevated risk.

**Decision**: [IN_SCOPE / OUT_OF_SCOPE]

**Rationale and evidence**:
- [Evidence with links to requirements, service process, and data model]

## 2A. Evidence Inventory and Quality

Use this section to prevent “paper compliance”. Prefer implemented, testable evidence over intention statements.

**Evidence quality rubric**:

- **Strong**: implemented control + measurable telemetry + operational process + test evidence.
- **Medium**: implemented control + partial telemetry/process.
- **Weak**: intent statements only.

| Evidence | Location | Quality (Strong/Medium/Weak) | What it supports |
|---|---|---|---|
| Requirements | `projects/[PROJECT]/ARC-[ID]-REQ-v*.md` | [ ] | [User need, constraints, NFRs, contestability] |
| Data model | `projects/[PROJECT]/ARC-[ID]-DATA-v*.md` | [ ] | [Data categories, PI handling, flows] |
| Risk register | `projects/[PROJECT]/ARC-[ID]-RISK-v*.md` | [ ] | [AI risks, treatments, owners] |
| PIA | `projects/[PROJECT]/ARC-[ID]-PIA-v*.md` | [ ] | [APP risks, mitigations] |
| Secure by design | `projects/[PROJECT]/ARC-[ID]-SECD-v*.md` | [ ] | [Security controls, evidence] |
| Architecture diagrams | `projects/[PROJECT]/diagrams/ARC-[ID]-DIAG-*.md` | [ ] | [Trust boundaries, data flows] |
| ADRs | `projects/[PROJECT]/decisions/ADR-*.md` | [ ] | [Decision rationale, trade-offs] |
| External reports | `projects/[PROJECT]/external/*` | [ ] | [Testing, audits, evaluations] |

## 3. Governance Accountability Structure

### 3.1 Accountable Officials (AO)
- AO role(s), delegation, and contact details.
- Confirmation DTA notification process is defined.

### 3.2 Accountable Use Case Owner (AUCO)
- Named AUCO, role scope, delegated responsibilities.
- Confirmation AUCO has AI policy/tool familiarity.

### 3.3 Governance forums
- [Board / Senior executive / AI risk committee]
- Review cadence: [Monthly / Quarterly / Annual minimum for high-risk]

## 4. Mandatory Policy Requirement Conformance

| Requirement | Status | Evidence | Gap / Action |
|---|---|---|---|
| Public AI transparency statement exists and is current | [Met/Partial/Not Met] | [AITS doc URL] | [Action] |
| Strategic position on AI adoption documented and communicated | [Met/Partial/Not Met] | [Strategy artifact] | [Action] |
| AO designated and DTA notification path established | [Met/Partial/Not Met] | [Gov memo] | [Action] |
| AUCO designated for this in-scope use case | [Met/Partial/Not Met] | [Register entry] | [Action] |
| Internal in-scope AI use case register implemented | [Met/Partial/Not Met] | [AIUR artifact] | [Action] |
| Responsible AI operational process established | [Met/Partial/Not Met] | [Process docs] | [Action] |
| Mandatory staff training implemented | [Met/Partial/Not Met] | [LMS evidence] | [Action] |
| AI impact assessment completed pre-deployment | [Met/Partial/Not Met] | [AIIA artifact] | [Action] |
| Monitoring + re-validation triggers defined | [Met/Partial/Not Met] | [Ops plan] | [Action] |
| High-risk governance + DTA reporting process defined (if applicable) | [Met/Partial/Not Met] | [Governance record] | [Action] |

## 5. AI Impact and Risk Summary

- **Inherent risk rating**: [Low / Medium / High]
- **Residual risk rating**: [Low / Medium / High]
- **Top 5 risks**:
  1. [Risk] – [Treatment owner/date]
  2. [Risk] – [Treatment owner/date]
  3. [Risk] – [Treatment owner/date]
  4. [Risk] – [Treatment owner/date]
  5. [Risk] – [Treatment owner/date]

## 6. Technical Standard Adoption Plan

| Lifecycle stage | Applicability | Key controls selected | Evidence location |
|---|---|---|---|
| Whole lifecycle | [Applicable/Conditional/N/A] | [Operational model, auditability, explainability] | [Link] |
| Design | [Applicable/Conditional/N/A] | [Risk modelling, non-AI alternatives] | [Link] |
| Data | [Applicable/Conditional/N/A] | [Data quality, lineage, privacy controls] | [Link] |
| Train | [Applicable/Conditional/N/A] | [Output suppression, bias testing] | [Link] |
| Evaluate | [Applicable/Conditional/N/A] | [Validation + fairness + reliability tests] | [Link] |
| Integrate/Deploy | [Applicable/Conditional/N/A] | [Release controls + rollback] | [Link] |
| Monitor | [Applicable/Conditional/N/A] | [Drift/safety/security/compliance monitoring] | [Link] |
| Decommission | [Applicable/Conditional/N/A] | [Retirement, data/system teardown, records retention] | [Link] |

## 7. Legal and Regulatory Interface

- Privacy Act / APP obligations identified: [Yes/No + detail]
- PIA requirement and status: [Required/Not Required + status]
- Administrative law and contestability obligations considered: [Yes/No + detail]
- FOI/records management considerations identified: [Yes/No + detail]
- PSPF/ISM obligations for OFFICIAL information and GenAI use addressed: [Yes/No + detail]

## 8. Decision and Approval

- **Assessment outcome**: [Proceed / Proceed with conditions / Do not proceed]
- **Conditions**:
  - [Condition 1]
  - [Condition 2]
- **Approving authority**: [Name/Role]
- **Decision date**: [YYYY-MM-DD]
- **Next mandatory review date**: [YYYY-MM-DD]

## 9. Action Plan

| Priority | Action | Owner | Due date | Dependency |
|---|---|---|---|---|
| High | [Action] | [Owner] | [Date] | [Dependency] |
| Medium | [Action] | [Owner] | [Date] | [Dependency] |
| Low | [Action] | [Owner] | [Date] | [Dependency] |

## 10. Source Traceability (Minimum)

| Assessment section | AU source anchor |
|---|---|
| In-scope determination | AI policy v2.0 Appendix C and mandatory assessment requirements |
| Accountability roles | Standard for accountability (AOs, AUCOs, register fields) |
| Transparency obligations | Standard for AI transparency statements |
| Risk assessment method | AI impact assessment tool + guidance |
| Technical controls | AI technical standard criteria |
| Privacy controls | OAIC AI/privacy guidance + PIA guide |
| Assurance model | Finance national AI assurance framework |
| Security handling | PSPF advisory + ISM/ACSC references |

## Appendix A: Operational Monitoring and Re-Validation Plan (Recommended)

This appendix keeps the assessment useful through-life (not just pre-deployment).

### A.1 Monitoring Coverage

| Area | What is monitored | Thresholds / triggers | Response owner | Evidence |
|---|---|---|---|---|
| Performance | [Metrics] | [Threshold] | [Role] | [Link] |
| Drift | [Signals] | [Threshold] | [Role] | [Link] |
| Safety | [Unsafe outputs/harms] | [Trigger] | [Role] | [Link] |
| Fairness | [Bias indicators] | [Trigger] | [Role] | [Link] |
| Security | [Prompt injection/data leakage] | [Trigger] | [Role] | [Link] |

### A.2 Re-Validation Triggers

- material change to model/provider/version
- material change to prompts/policies/guardrails
- material change to data sources or data classification/handling
- material change to decision authority / human oversight model
- material incident or harm event
- scheduled periodic review date: [YYYY-MM-DD]

## Appendix B: AI-Specific Threats and Controls (Recommended)

| Threat | Example | Controls | Evidence | Residual risk |
|---|---|---|---|---|
| Prompt injection / jailbreak | [Example] | [Controls] | [Link] | [L/M/H] |
| Data leakage | [Example] | [Controls] | [Link] | [L/M/H] |
| Data poisoning | [Example] | [Controls] | [Link] | [L/M/H] |
| Model supply chain risk | [Example] | [Controls] | [Link] | [L/M/H] |
| Over-reliance/automation bias | [Example] | [Controls] | [Link] | [L/M/H] |
