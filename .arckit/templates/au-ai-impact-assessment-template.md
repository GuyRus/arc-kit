# AU AI Impact Assessment

> **Template Status**: Stable | **Version**: [VERSION] | **Primary reference**: DTA AI impact assessment tool + guidance PDF

## Document control

| Field | Value |
|---|---|
| Document ID | ARC-[PROJECT_ID]-AIIA-v[VERSION] |
| Project | [PROJECT_NAME] |
| Lead agency | [ENTITY] |
| Assessing officer | [NAME/ROLE/EMAIL] |
| Approving officer | [NAME/ROLE/EMAIL] |
| Accountable use case owner | [NAME/ROLE/EMAIL] |
| Assessment status | [Draft / Approved / Re-validation in progress] |
| Last updated | [YYYY-MM-DD] |

## Policy baseline references

| Source | Purpose |
|---|---|
| Policy for the responsible use of AI in government 2.0 | Defines mandatory governance obligations for in-scope Australian Government AI use cases. |
| Guidance for the AI impact assessment tool (PDF) | Provides the canonical 12-section assessment method and risk workflow used by this template. |
| Australian Government AI technical standard | Provides lifecycle technical controls used to design treatments and monitoring actions. |

## Evidence Inventory and Quality (Recommended)

Prefer implemented, testable evidence over intention statements. If evidence is missing, record a `TODO` and an action (do not invent).

**Evidence quality rubric**:

- **Strong**: implemented control + measurable telemetry + operational process + test evidence.
- **Medium**: implemented control + partial telemetry/process.
- **Weak**: intent statements only.

| Evidence | Location | Quality (Strong/Medium/Weak) | What it supports |
|---|---|---|---|
| Use case register | `ARC-[PROJECT_ID]-AIUR-v[VERSION].md` | [ ] | [Accountability and minimum fields] |
| Governance assessment | `ARC-[PROJECT_ID]-AIGA-v[VERSION].md` | [ ] | [Policy obligations and approvals] |
| Requirements | `ARC-[PROJECT_ID]-REQ-v*.md` | [ ] | [User needs, decision points, contestability] |
| Data model | `ARC-[PROJECT_ID]-DATA-v*.md` | [ ] | [Data categories, PI handling, flows] |
| Risk register | `ARC-[PROJECT_ID]-RISK-v*.md` | [ ] | [Risks, treatments, owners] |
| PIA | `ARC-[PROJECT_ID]-PIA-v*.md` | [ ] | [APP risks, mitigations] |
| Secure by design | `ARC-[PROJECT_ID]-SECD-v*.md` | [ ] | [Security controls, evidence] |
| Architecture diagrams | `diagrams/ARC-[PROJECT_ID]-DIAG-*.md` | [ ] | [Trust boundaries, data flows] |
| External evaluations | `external/*` | [ ] | [Testing, audits, model evaluation] |

---

## Section 1 — Basic information

### 1.1 AI use case profile
- Name of AI use case: [TEXT]
- Internal reference number: [TEXT]
- Lead agency: [TEXT]

### 1.2 Responsibilities
- Assessing officer: [TEXT]
- Approving officer: [TEXT]
- Accountable use case owner(s): [TEXT]
- Additional roles/responsibilities: [TEXT]

### 1.3 Use case description
Plain-language summary of intended AI use, expected outcome, and boundaries.

### 1.4 In-scope determination (Policy Appendix C)
Tick all that apply:
- [ ] Potential for more than insignificant harm
- [ ] Material influence on administrative decisions
- [ ] Public interaction/significant impact without human review
- [ ] Uses personal/sensitive/security-classified data
- [ ] Elevated risk directed by DTA
- [ ] Not applicable

### 1.5 Technology and classification
- Type(s) of AI technology: [TEXT]
- Usage pattern(s): [TEXT]
- Domain(s): [TEXT]
- Administrative decision automation authority (if relevant): [TEXT]

### 1.6 Expert contributions
| Expert | Role/expertise | Date consulted | Input and resulting change |
|---|---|---|---|
| [Name] | [Role] | [Date] | [Summary] |

### 1.7 Review log
| Review type | Reason | Date | Post-review changes |
|---|---|---|---|
| Pre-deployment / Re-validation | [Reason] | [Date] | [Summary] |

---

## Section 2 — Purpose and expected benefits

### 2.1 Problem definition
[Problem being solved]

### 2.2 AI use case purpose
[How AI addresses the problem]

### 2.3 Non-AI alternatives
[Alternatives considered and rationale]

### 2.4 Stakeholder mapping
| Stakeholder group | How they may be affected |
|---|---|
| [Group] | [Impact] |

### 2.5 Expected benefits
[Quantitative and/or qualitative benefits with assumptions]

---

## Section 3 — Inherent risk assessment

Use DTA consequence + likelihood method.

| Risk area | Consequence | Likelihood | Inherent rating | Rationale |
|---|---|---|---|---|
| Accessibility and inclusion | [Insig/Minor/Moderate/Major/Severe] | [Rare/Unlikely/Possible/Likely/Almost certain] | [Low/Medium/High] | [Text] |
| Fairness/discrimination | ... | ... | ... | ... |
| Reliability/safety | ... | ... | ... | ... |
| Privacy | ... | ... | ... | ... |
| Security | ... | ... | ... | ... |
| Transparency/explainability | ... | ... | ... | ... |
| Contestability/administrative justice | ... | ... | ... | ... |
| Human rights/human-centred impacts | ... | ... | ... | ... |

### 3.9 Overall inherent risk rating
[Low / Medium / High]

---

## Section 4 — Threshold assessment outcome

### 4.1 Assessing officer recommendation
- [ ] Full assessment required
- [ ] Full assessment not required

### 4.2 Approving officer review
- Decision: [Approved / Not approved]
- Rationale: [Text]

---

## Section 5 — Fairness

- Fairness definition for this use case.
- Protected groups potentially affected.
- Bias testing design and acceptance thresholds.
- Bias mitigations and residual limitations.

| Fairness check | Method | Result | Action required |
|---|---|---|---|
| [Check] | [Method] | [Result] | [Action] |

---

## Section 6 — Reliability and safety

- Data suitability and representativeness.
- Testing regime (functional, robustness, edge cases, failure modes).
- Pilot evidence and readiness criteria.
- Monitoring plan and intervention controls.
- Operator training and preparedness to disengage.

---

## Section 7 — Privacy protection and security

- Data minimisation and handling controls.
- Privacy threshold/impact assessment status.
- APP obligations and lawful handling rationale.
- Security controls (PSPF/ISM/ACSC aligned).

---

## Section 8 — Transparency and explainability

- Consultation approach.
- Public visibility/disclosure approach.
- Documentation and records strategy.
- Explanation strategy for affected people and staff.

---

## Section 9 — Contestability

- Notification to people when AI affects rights/outcomes.
- Challenge/review pathways and service levels.
- Escalation path to human decision-maker.

---

## Section 10 — Human-centred values

- Diversity/inclusion considerations embedded in design and operations.
- Human rights and societal impact considerations.

---

## Section 11 — Accountability

- End-to-end lifecycle accountability model.
- Decision logging and audit evidence.
- Governance reporting cadence.

---

## Section 12 — Residual risk and next steps

### 12.1 Legal framework alignment
[Summary]

### 12.2 Legal advice status
[Obtained / Pending / Not required + rationale]

### 12.3 Risk treatment summary
| Medium/High inherent risk | Treatment | Owner | Due date | Status |
|---|---|---|---|---|
| [Risk] | [Treatment] | [Owner] | [Date] | [Status] |

### 12.4 Overall residual risk rating
[Low / Medium / High]

### 12.5 Governance body review (required for high-risk)
- Governing body / senior executive outcome: [Text]
- DTA reporting status (for inherent high-risk): [Text]

### 12.6 Re-validation triggers
- Material scope change
- Material usage change
- Material operational/vendor/regulatory change
- Scheduled periodic review date: [YYYY-MM-DD]
