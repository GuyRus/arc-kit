# Project Plan Playbook

`/arckit.plan` creates an AU Commonwealth-aligned delivery plan with phases, gates, dependencies, and Mermaid timelines.

---

## Inputs

| Artefact | Purpose |
|----------|---------|
| Stakeholder analysis & principles | Populate governance roles and success criteria |
| Risk register & business case | Feed gate actions and critical path |
| Requirements overview | Determines key activities across phases |

### AU policy baseline for planning

- Digital Experience Policy and Digital Service Standard
- Finance assurance review expectations (Gateway/IRA where applicable)
- Commonwealth Procurement Rules (CPRs)
- Privacy Act 1988 + APPs
- PSPF + ASD ISM

---

## Command

```bash
/arckit.plan Create project plan for <initiative>
```

Output: `projects/<id>/ARC-<id>-PLAN-v1.0.md` plus Mermaid diagrams.

---

## Plan Structure

| Section | Contents |
|---------|----------|
| Timeline overview | Discovery → Alpha → Beta → Live with dates and milestones |
| Phase detail | Activities, deliverables, owners, entry/exit criteria |
| Gate checklist | Evidence required for Discovery/Alpha/Beta/Live gates and AU assurance checkpoints |
| Dependency matrix | ArcKit commands sequenced with predecessors |
| Risk & mitigation | Key timeline threats with contingency |

---

## One-Page Workflow

| Phase | Key Activities | ArcKit Commands |
|-------|----------------|-----------------|
| Discovery | Stakeholders, problem framing, initial business case | `/arckit.stakeholders`, `/arckit.principles`, `/arckit.sobc` |
| Alpha | Detailed requirements, architecture, procurement | `/arckit.requirements`, `/arckit.diagram`, `/arckit.sow`, `/arckit.hld-review` |
| Beta | Build, test, operational readiness | `/arckit.dld-review`, `/arckit.backlog`, `/arckit.analyze`, `/arckit.servicenow` |
| Live | Go-live, transition to BAU, continuous improvement | `/arckit.story`, `/arckit.traceability`, `/arckit.analyze` (cadence) |

---

## Review Checklist

- Phases align to Digital Experience Policy / Digital Service Standard and organisational governance.
- Each gate lists approvers and evidence (business case, design review, PIA).
- Dependencies cover AU compliance artefacts (CPRs, Privacy/APP, PSPF/ISM, AI Playbook where relevant).
- Buffer time included for procurement, assurance, and change freeze windows.
- Risks highlight delivery blockers (supplier delay, funding approval, staffing).

---

## Updating the Plan

- Refresh monthly and after major decisions; version documents in git.
- Share Mermaid Gantt to stakeholders via docs or static site.
- Feed changes into `/arckit.story` to capture project history.
