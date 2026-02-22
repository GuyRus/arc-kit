# Digital Service Standard (DSS) Assurance Prep Report

> **Template Status**: Beta | **Version**: [VERSION] | **Command**: `/arckit.service-assessment`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-[PROJECT_ID]-SVCASS-v[VERSION] |
| **Document Type** | Digital Service Standard (DSS) Assurance Prep Report |
| **Project** | [PROJECT_NAME] (Project [PROJECT_ID]) |
| **Classification** | [PUBLIC / OFFICIAL / OFFICIAL:Sensitive / PROTECTED / SECRET / TOP SECRET] |
| **Status** | [DRAFT / IN_REVIEW / APPROVED / PUBLISHED / SUPERSEDED / ARCHIVED] |
| **Version** | [VERSION] |
| **Created Date** | [YYYY-MM-DD] |
| **Last Modified** | [YYYY-MM-DD] |
| **Review Cycle** | [Monthly / Quarterly / Annual / On-Demand] |
| **Next Review Date** | [YYYY-MM-DD] |
| **Owner** | [OWNER_NAME_AND_ROLE] |
| **Reviewed By** | [REVIEWER_NAME] ([YYYY-MM-DD]) or PENDING |
| **Approved By** | [APPROVER_NAME] ([YYYY-MM-DD]) or PENDING |
| **Distribution** | [DISTRIBUTION_LIST] |
| **Delivery Stage** | [Discovery / Alpha / Beta / Live] |
| **Review Date** | [Date / Not yet scheduled] |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| [VERSION] | [DATE] | ArcKit AI | Initial creation from `/arckit.service-assessment` command | PENDING | PENDING |

---

## Executive Summary

**Overall Readiness**: [🟢 Green / 🟡 Amber / 🔴 Red]

**Readiness Score**: [X]/10 criteria ready

**Breakdown**:
- 🟢 Green: [X] criteria
- 🟡 Amber: [X] criteria
- 🔴 Red: [X] criteria

**Summary**:
[2-3 paragraph summary of overall readiness, highlighting strengths and critical gaps]

**Critical Gaps** (Must address before review):
- [Gap 1 with DSS criterion number]
- [Gap 2 with DSS criterion number]
- [Gap 3 with DSS criterion number]

**Key Strengths**:
- [Strength 1]
- [Strength 2]
- [Strength 3]

**Recommended Timeline**:
[X weeks/days until ready based on gap analysis]
[If review date provided: "Review in X days - [Ready/Need to postpone]"]

---

## DSS Criteria Assessment (10)

For each criterion, capture what it means, evidence, gaps, and actions.

### Stage Expectations (How Much Evidence Is “Enough”)

Use the **Delivery Stage** to tune what “Ready” means.

- **Discovery**: intent clarity, user understanding, inclusion risks, service ecosystem, early trust/harm analysis, early operating model assumptions.
- **Alpha**: prototypes and spikes, early integration approach, early security/privacy-by-design, measurement approach defined, decisions recorded.
- **Beta**: implementation evidence, operating model more concrete, monitoring and incident readiness, assurance/testing evidence, operational acceptance path.
- **Live**: service is operating, performance and outcomes measured, continuous improvement demonstrated, governance cadence in place, known risks actively managed.

### 1. Have Clear Intent

**Status**: [🟢 Ready / 🟡 Partial / 🔴 Not Ready]

**Intent Statement**:
[One paragraph: the service intent, outcome, and what success means]

**Evidence Found**:
- [Evidence in requirements / stakeholders / business case]

**Gaps**:
- [Missing or weak evidence]

**Recommendations**:
- [Action, timeline, owner, evidence to create]

**Stage-specific expectations** (tailor to context; do not invent evidence):

- **Discovery**: [ ] clear service intent and problem statement; [ ] success measures identified; [ ] scope and out-of-scope captured
- **Alpha**: [ ] intent validated with stakeholders/users; [ ] MVP boundaries defined; [ ] key decisions recorded (ADRs where relevant)
- **Beta**: [ ] intent reflected in delivery plan/roadmap; [ ] measures have baselines; [ ] trade-offs documented and accepted
- **Live**: [ ] measures reviewed on a cadence; [ ] outcomes and learnings inform change; [ ] ownership for ongoing relevance is explicit

---

### 2. Know Your User

**Status**: [🟢 Ready / 🟡 Partial / 🔴 Not Ready]

**Evidence Found**:
- [User needs and research, personas, journey mapping]

**Gaps**:
- [Missing research, weak synthesis, unvalidated assumptions]

**Recommendations**:
- [Action, timeline, owner, evidence to create]

**Stage-specific expectations** (tailor to context; do not invent evidence):

- **Discovery**: [ ] primary user groups identified; [ ] initial user needs captured; [ ] research plan exists
- **Alpha**: [ ] prototypes tested with representative users; [ ] needs updated from findings; [ ] journey/service blueprint draft exists
- **Beta**: [ ] usability testing occurs regularly; [ ] analytics supports user-need hypotheses; [ ] pain points tracked and addressed
- **Live**: [ ] feedback loops active; [ ] user satisfaction and completion metrics tracked; [ ] issues backlog shows continuous improvement

---

### 3. Leave No One Behind

**Status**: [🟢 Ready / 🟡 Partial / 🔴 Not Ready]

**Evidence Found**:
- [Accessibility approach, WCAG evidence, inclusive design considerations]

**Gaps**:
- [Missing testing, missing accessibility NFRs, missing assistive tech coverage]

**Recommendations**:
- [Action, timeline, owner, evidence to create]

**Stage-specific expectations** (tailor to context; do not invent evidence):

- **Discovery**: [ ] inclusion risks identified; [ ] accessibility requirements captured; [ ] assisted-digital needs considered
- **Alpha**: [ ] designs/prototypes reviewed for accessibility; [ ] content and language tested; [ ] early WCAG approach defined
- **Beta**: [ ] accessibility testing evidence exists (incl. assistive tech where relevant); [ ] defects tracked and remediated
- **Live**: [ ] accessibility monitored; [ ] content/governance keeps service inclusive; [ ] escalation and remediation processes exist

---

### 4. Connect Services

**Status**: [🟢 Ready / 🟡 Partial / 🔴 Not Ready]

**Evidence Found**:
- [Integration requirements, ecosystem map, cross-agency dependencies]

**Gaps**:
- [Unowned integrations, unclear data flows, missing operational responsibilities]

**Recommendations**:
- [Action, timeline, owner, evidence to create]

**Stage-specific expectations** (tailor to context; do not invent evidence):

- **Discovery**: [ ] service ecosystem mapped; [ ] integration assumptions captured; [ ] dependencies and owners identified (even if provisional)
- **Alpha**: [ ] integration approach prototyped/spiked; [ ] data sharing constraints identified; [ ] operational responsibilities drafted
- **Beta**: [ ] integrations implemented or delivery-ready; [ ] interface contracts documented; [ ] failure modes and support model defined
- **Live**: [ ] integrations monitored; [ ] change management exists for upstream/downstream changes; [ ] incidents and improvements tracked

---

### 5. Build Trust In Design

**Status**: [🟢 Ready / 🟡 Partial / 🔴 Not Ready]

**Evidence Found**:
- [Security-by-design evidence, privacy-by-design evidence, user trust measures]

**Gaps**:
- [Missing threat model, unclear identity approach, weak auditability]

**Recommendations**:
- [Action, timeline, owner, evidence to create]

**Stage-specific expectations** (tailor to context; do not invent evidence):

- **Discovery**: [ ] trust risks identified (security/privacy/fraud); [ ] early controls and policy constraints documented
- **Alpha**: [ ] identity and access approach designed; [ ] threat modelling started for key flows; [ ] privacy impacts assessed where relevant
- **Beta**: [ ] security testing evidence exists; [ ] logging/monitoring approach implemented; [ ] privacy controls implemented per PIA actions
- **Live**: [ ] controls operating; [ ] incident readiness demonstrated; [ ] auditability and governance cadence maintained

---

### 6. Don’t Reinvent The Wheel

**Status**: [🟢 Ready / 🟡 Partial / 🔴 Not Ready]

**Evidence Found**:
- [Reuse of platforms/components, build vs buy decisions, shared services]

**Gaps**:
- [Duplicated capability, missing rationale for bespoke build]

**Recommendations**:
- [Action, timeline, owner, evidence to create]

**Stage-specific expectations** (tailor to context; do not invent evidence):

- **Discovery**: [ ] existing platforms/components reviewed; [ ] reuse options identified; [ ] build vs buy questions logged
- **Alpha**: [ ] prototypes/spikes compare reuse vs bespoke; [ ] decision criteria defined; [ ] costs/constraints captured
- **Beta**: [ ] reuse integrated where chosen; [ ] bespoke build rationale documented; [ ] operational ownership and support considered
- **Live**: [ ] reuse continues to be reviewed; [ ] technical debt is visible; [ ] platform alignment is maintained

---

### 7. Do No Harm

**Status**: [🟢 Ready / 🟡 Partial / 🔴 Not Ready]

**Evidence Found**:
- [Risk analysis, mitigations, privacy impacts, safety and integrity controls]

**Gaps**:
- [Unmitigated risks, missing incident response readiness, missing safeguards]

**Recommendations**:
- [Action, timeline, owner, evidence to create]

**Stage-specific expectations** (tailor to context; do not invent evidence):

- **Discovery**: [ ] harms and risks identified (privacy, security, safety, integrity); [ ] mitigations proposed; [ ] escalation/decision path identified
- **Alpha**: [ ] safeguards designed (human oversight where needed); [ ] monitoring approach planned; [ ] PIA/risk mitigations tracked
- **Beta**: [ ] safeguards implemented and tested; [ ] incident response and rollback procedures exist; [ ] residual risk acceptance documented
- **Live**: [ ] harms monitored; [ ] incidents and near-misses reviewed; [ ] continuous improvement reduces risk over time

---

### 8. Innovate With Purpose

**Status**: [🟢 Ready / 🟡 Partial / 🔴 Not Ready]

**Evidence Found**:
- [Why innovation is needed, measurable value, experiments and learnings]

**Gaps**:
- [Innovation without value case, missing evaluation plan]

**Recommendations**:
- [Action, timeline, owner, evidence to create]

**Stage-specific expectations** (tailor to context; do not invent evidence):

- **Discovery**: [ ] innovation hypothesis linked to user need/outcome; [ ] baseline/measurement approach defined; [ ] constraints and risks considered
- **Alpha**: [ ] experiments are run and documented; [ ] learning log shows pivots; [ ] decisions recorded based on evidence
- **Beta**: [ ] innovation is operationalised (feature flags, controlled rollouts); [ ] measures show impact; [ ] cost/benefit tracked
- **Live**: [ ] innovation is governed; [ ] changes are evaluated; [ ] learnings inform roadmap and continuous improvement

---

### 9. Monitor Your Service

**Status**: [🟢 Ready / 🟡 Partial / 🔴 Not Ready]

**Evidence Found**:
- [SLIs/SLOs, dashboards, alerting, incident processes, operational readiness]

**Gaps**:
- [Missing SLOs, unclear on-call, no runbooks]

**Recommendations**:
- [Action, timeline, owner, evidence to create]

**Stage-specific expectations** (tailor to context; do not invent evidence):

- **Discovery**: [ ] success measures identified; [ ] monitoring approach outlined; [ ] operational ownership assumptions captured
- **Alpha**: [ ] logging/telemetry design exists; [ ] initial dashboards/probes prototyped; [ ] SLI/SLO candidates identified
- **Beta**: [ ] monitoring implemented; [ ] alerts and runbooks exist; [ ] incident/change processes are defined and exercised
- **Live**: [ ] metrics reviewed on cadence; [ ] service performance and outcomes reported; [ ] incidents drive improvements

---

### 10. Keep It Relevant

**Status**: [🟢 Ready / 🟡 Partial / 🔴 Not Ready]

**Evidence Found**:
- [Governance cadence, review cycles, continuous improvement mechanisms]

**Gaps**:
- [No review cadence, no ownership, stale assumptions]

**Recommendations**:
- [Action, timeline, owner, evidence to create]

**Stage-specific expectations** (tailor to context; do not invent evidence):

- **Discovery**: [ ] ownership and governance for decisions is identified; [ ] review points planned; [ ] assumptions logged
- **Alpha**: [ ] roadmap reflects learnings; [ ] governance cadence defined; [ ] decisions updated as evidence changes
- **Beta**: [ ] regular reviews occur (risks, measures, user needs); [ ] technical debt is tracked; [ ] changes are controlled
- **Live**: [ ] continuous improvement loop exists; [ ] service remains current (policy/tech/user expectations); [ ] retirement/transition plans exist

---

## Evidence Inventory

**Traceability**: DSS Criterion → ArcKit Artefacts

| DSS Criterion | ArcKit Artefacts | Status | Critical Gaps |
|--------------|------------------|--------|---------------|
| 1. Have clear intent | [artefacts] | [🟢/🟡/🔴] | [gaps] |
| 2. Know your user | [artefacts] | [🟢/🟡/🔴] | [gaps] |
| 3. Leave no one behind | [artefacts] | [🟢/🟡/🔴] | [gaps] |
| 4. Connect services | [artefacts] | [🟢/🟡/🔴] | [gaps] |
| 5. Build trust in design | [artefacts] | [🟢/🟡/🔴] | [gaps] |
| 6. Don’t reinvent the wheel | [artefacts] | [🟢/🟡/🔴] | [gaps] |
| 7. Do no harm | [artefacts] | [🟢/🟡/🔴] | [gaps] |
| 8. Innovate with purpose | [artefacts] | [🟢/🟡/🔴] | [gaps] |
| 9. Monitor your service | [artefacts] | [🟢/🟡/🔴] | [gaps] |
| 10. Keep it relevant | [artefacts] | [🟢/🟡/🔴] | [gaps] |

---

## Action Plan

### Critical Actions (0-2 weeks)

- [ ] [Action] (Criterion: [N])
- [ ] [Action] (Criterion: [N])

### High Priority Actions (2-6 weeks)

- [ ] [Action] (Criterion: [N])

### Medium Priority Actions (Nice to have)

- [ ] [Action] (Criterion: [N])

---

## Assurance Review Session Guidance

Use this section to run an assurance review that is proportionate and evidence-based.

### Suggested Attendees

- Service owner / product lead
- Delivery lead
- User researcher / content (as applicable)
- Technical architect / engineering lead
- Security / privacy SMEs (where applicable)
- Operations / service management

### Suggested Agenda

1. Service intent and scope (Criterion 1)
2. Users and inclusion (Criteria 2-3)
3. Service ecosystem and reuse (Criteria 4 and 6)
4. Trust, safety, and harm controls (Criteria 5 and 7)
5. Innovation rationale (Criterion 8)
6. Monitoring and relevance (Criteria 9-10)
7. Gaps, actions, and owners

---

**Generated by**: ArcKit `/arckit.service-assessment` command
**Generated on**: [DATE]
**ArcKit Version**: [VERSION]
**Project**: [PROJECT_NAME]
**Model**: [AI_MODEL]
