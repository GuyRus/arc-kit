# AU Defence AI Assurance Pathway (Public-source baseline)

> **Template Status**: Transitional | **Version**: [VERSION] | **Command**: `/arckit.jsp-936`

## Important Scope Note

No current publicly discoverable Australian Defence-wide equivalent to UK MOD JSP 936 was identified in the AU policy corpus used for this rewrite.

This template therefore provides a **public-source AU baseline pathway** and explicitly records internal Defence dependencies as `SOURCE_GAP` items.

The intent is to keep this document **useful and reusable** even when internal Defence assurance processes differ.

---

## Document Control

| Field | Value |
|---|---|
| Document ID | ARC-[PROJECT_ID]-ADEF-v[VERSION] |
| Document Type | AU Defence AI Assurance Pathway (Public-source baseline) |
| Project | [PROJECT_NAME] (Project [PROJECT_ID]) |
| Classification | [PUBLIC / OFFICIAL / OFFICIAL:Sensitive / PROTECTED / SECRET / TOP SECRET] |
| Status | [DRAFT / IN_REVIEW / APPROVED / PUBLISHED / SUPERSEDED / ARCHIVED] |
| Version | [VERSION] |
| Created date | [YYYY-MM-DD] |
| Last modified | [YYYY-MM-DD] |
| Review cycle | [Monthly / Quarterly / Annual / On-Demand] |
| Next review date | [YYYY-MM-DD] |
| Owner | [OWNER_NAME_AND_ROLE] |
| Reviewed by | [REVIEWER_NAME] ([YYYY-MM-DD]) or PENDING |
| Approved by | [APPROVER_NAME] ([YYYY-MM-DD]) or PENDING |
| Distribution | [DISTRIBUTION_LIST] |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---|---|---|---|---|---|
| [VERSION] | [YYYY-MM-DD] | ArcKit AI | Initial creation from `/arckit.jsp-936` | PENDING | PENDING |

---

## Executive Summary

**AI capability / use case**: [NAME]

**Operational context**: [Defence / Defence-adjacent / national security / enabling capability]

**AI technology type**: [GenAI / ML / NLP / CV / Hybrid]

**Decision authority**: [Advisory / Decision support / Human decision-maker required / Automated action]

**Human oversight model**: [Human-in-the-loop / Human-on-the-loop / Human-in-command]

**Highest information classification handled**: [PUBLIC / OFFICIAL / OFFICIAL:Sensitive / PROTECTED / SECRET / TOP SECRET]

**Overall assurance readiness**: [Ready / Not ready / Ready with conditions]

**Top assurance gaps (blockers)**:

| # | Gap | Impact | Owner | Due date |
|---|---|---|---|---|
| 1 | [Gap] | [Impact] | [Role] | [YYYY-MM-DD] |
| 2 | [Gap] | [Impact] | [Role] | [YYYY-MM-DD] |
| 3 | [Gap] | [Impact] | [Role] | [YYYY-MM-DD] |

---

## 1. Public-Source Policy Context

| Topic | Public source anchor | Practical implication |
|---|---|---|
| DTA AI policy carveout for defence portfolio | DTA AI policy v2.0 – national security carveouts | Whole-of-government AI policy may not apply directly to defence contexts; where adopted, record how and why. |
| OFFICIAL information and GenAI | PSPF Policy Advisory 001-2025 | Defines provider constraints and PSPF authorisation expectations for GenAI in OFFICIAL contexts. |
| Secure AI development practices | ACSC secure AI guidance | Provides secure lifecycle controls for design, development, deployment, and operations. |
| Information security baselines | ISM + PSPF references | Security controls and authorisation pathways remain mandatory in relevant contexts. |

---

## 2. System and AI Boundary

### 2.1 System Overview

- **System purpose**: [What problem is solved]
- **Operational users**: [Who uses the system and how]
- **Operating environment**: [Connected/disconnected; constrained networks; edge/cloud/on-prem]
- **Fallback mode**: [What happens if AI is unavailable or unsafe]

### 2.2 AI Component Inventory

| Component | Type | Purpose | Inputs | Outputs | Human control points | Supplier/Owner | Notes |
|---|---|---|---|---|---|---|---|
| [Component] | [GenAI/ML/etc] | [Purpose] | [Inputs] | [Outputs] | [Controls] | [Owner] | [Notes] |

### 2.3 Data Sources and Handling Summary

- **Data sources**: [Systems/datasets]
- **Personal information**: [Yes/No + summary]
- **Sensitive/security-classified information**: [Yes/No + summary]
- **Data minimisation**: [Approach]
- **Data retention and disposal**: [Approach]

---

## 3. Assurance Approach (Baseline)

This section provides a generic, reusable assurance approach that can be mapped to internal Defence policy and governance forums.

### 3.1 Useful Organising Lenses (Optional)

Use these lenses where they add clarity. Do not claim they are mandated unless evidenced:

- **Secure by Design principles**: establish context, security-from-start, defence in depth, secure patterns, continuous risk management, supply chain security, through-life assurance.
- **NIST Cybersecurity Framework** (optional): Identify / Protect / Detect / Respond / Recover.
- **Three Lines of Defence** (optional): delivery ownership, assurance/oversight, independent review/audit.

### 3.2 Evidence Quality Rubric

- **Strong**: implemented control + measurable telemetry + operational process + test evidence.
- **Medium**: implemented control + partial telemetry/process.
- **Weak**: intent statements only.

---

## 4. Assurance Lifecycle Plan (Through-Life)

Use this to define gates, required evidence, and exit criteria.

| Stage | Goal | Minimum evidence | Exit criteria |
|---|---|---|---|
| Discover / Plan | Define intent, boundaries, risks, governance | use case profile; data classification; initial risk assessment; governance roles | in-scope decision; assurance plan agreed |
| Design | Design safeguards and oversight | architecture + trust boundaries; threat model (as applicable); human oversight design | key controls designed; decisions recorded |
| Build / Configure | Implement controls | secure SDLC evidence; guardrails; logging; access controls | controls implemented; test plan approved |
| Test / Evaluate | Validate safety/reliability/fairness/security | evaluation results; red team/abuse testing (as applicable); privacy/security testing | acceptance criteria met or exceptions recorded |
| Deploy | Controlled rollout | release/rollback plan; operator training; incident playbooks | operational readiness confirmed |
| Operate | Monitor and improve | monitoring dashboards; incident response; re-validation triggers | service operating within thresholds |
| Retire | Safe decommission | retirement plan; records retention; teardown evidence | AI capability retired safely |

---

## 5. Core Assurance Domains (Assessment)

Use statuses: ✅ Achieved / ⚠️ Partially Achieved / ❌ Not Achieved / N/A.

### 5.1 Governance, Decision Rights, and Risk Acceptance

**Status**: [✅/⚠️/❌/N/A]

**Evidence**:
- [Links]

**Findings**:
- [Finding]

**Actions**:
- [Action] (Owner: [Role], Due: [YYYY-MM-DD])

### 5.2 Human Oversight and Contestability

**Status**: [✅/⚠️/❌/N/A]

Include:

- where human review is required vs optional
- intervention/disengagement mechanisms and triggers
- operator training and workload implications
- notification and contestability mechanisms (where relevant)

### 5.3 Data Governance and Privacy (If Applicable)

**Status**: [✅/⚠️/❌/N/A]

Include:

- data minimisation and handling constraints
- privacy impact assessment status (where relevant)
- access logging and auditing for sensitive datasets

### 5.4 Safety, Reliability, and Performance

**Status**: [✅/⚠️/❌/N/A]

Include:

- acceptance criteria and evaluation metrics
- failure modes and safe defaults
- robustness testing and operational constraints

### 5.5 Fairness and Human-Centred Impacts

**Status**: [✅/⚠️/❌/N/A]

Include:

- affected groups and potential harms
- bias testing approach and limitations
- mitigations and residual risk

### 5.6 Transparency and Records Management

**Status**: [✅/⚠️/❌/N/A]

Include:

- records strategy (inputs/outputs/decisions)
- explanation approach for users/decision-makers
- FOI/records considerations (where applicable)

### 5.7 Security and Secure Engineering (AI-Specific)

**Status**: [✅/⚠️/❌/N/A]

Include:

- prompt injection/jailbreak risks (GenAI)
- data leakage risks
- model and dependency supply chain risks
- secure SDLC controls and build integrity evidence

### 5.8 Monitoring, Incidents, and Re-Validation

**Status**: [✅/⚠️/❌/N/A]

Include:

- drift/safety/fairness/security monitoring
- incident response playbooks for AI harms
- re-validation triggers and review cadence

---

## 6. Assurance Evidence Checklist (Minimum)

Tick what exists and link evidence.

| Area | Evidence item | Status | Link |
|---|---|---|---|
| Boundary | AI component inventory and decision points | [ ] | [ ] |
| Data | Data sources + classification + handling rules | [ ] | [ ] |
| Governance | Roles, decision rights, residual risk acceptance path | [ ] | [ ] |
| Testing | Evaluation plan and results | [ ] | [ ] |
| Safety | Safeguards and intervention/disengagement mechanisms | [ ] | [ ] |
| Security | Threat model + secure SDLC evidence | [ ] | [ ] |
| Operations | Monitoring + incident response playbooks | [ ] | [ ] |
| Change | Re-validation triggers and review cadence | [ ] | [ ] |
| Records | Decision logging and records retention approach | [ ] | [ ] |

---

## 7. SOURCE_GAP Register (Internal Defence Overlay Required)

Use this register to capture internal Defence-only dependencies that must be confirmed.

| Gap | Why it matters | Owner | Due date | Status |
|---|---|---|---|---|
| [SOURCE_GAP] Internal Defence AI risk taxonomy and risk appetite | Defines risk thresholds and required governance route | [Role] | [YYYY-MM-DD] | [Open/Closed] |
| [SOURCE_GAP] Approval authority chain for AI capability release | Determines sign-off forums and evidence requirements | [Role] | [YYYY-MM-DD] | [Open/Closed] |
| [SOURCE_GAP] Defence incident reporting doctrine for AI harms | Determines notification, escalation, and reporting | [Role] | [YYYY-MM-DD] | [Open/Closed] |
| [SOURCE_GAP] Defence-specific ethical review process | Determines additional review steps and evidence | [Role] | [YYYY-MM-DD] | [Open/Closed] |

---

## 8. Traceability (Recommended)

| Item | Reference |
|---|---|
| Requirements | `ARC-[PROJECT_ID]-REQ-v*.md` |
| Data model | `ARC-[PROJECT_ID]-DATA-v*.md` |
| Risk register | `ARC-[PROJECT_ID]-RISK-v*.md` |
| Secure by design | `ARC-[PROJECT_ID]-SECD-v*.md` |
| PIA | `ARC-[PROJECT_ID]-PIA-v*.md` |
| AI governance assessment (AIGA) | `ARC-[PROJECT_ID]-AIGA-v*.md` |
| AI impact assessment (AIIA) | `ARC-[PROJECT_ID]-AIIA-v*.md` |
| AI transparency statement (AITS) | `ARC-[PROJECT_ID]-AITS-v*.md` |

---

## 9. Legacy UK Reference (Read-Only)

If a project explicitly requires historical UK JSP 936 structure for comparison/migration, use:

- `.arckit/templates/legacy-uk/jsp-936-template.md`

This is a **legacy reference only**, not an AU default artifact.

