# High-Level Design Review Playbook

`/arckit.hld-review` reviews a High-Level Design (HLD) against architecture principles, requirements, and governance standards.

---

## Inputs

| Artefact | Purpose |
|----------|---------|
| High-Level Design (HLD) | The design document being reviewed |
| Architecture principles | Governance standards to verify against |
| Requirements (`ARC-<id>-REQ-v1.0.md`) | Verify all requirements addressed |
| Risk register | Ensure risks are mitigated in design |
| Service/policy assessment (where applicable) | Digital Service Standard / technology-policy findings that the design must satisfy |
| Privacy and security artefacts (where available) | PIA findings, Secure by Design assessment, security control expectations |

---

## Command

```bash
/arckit.hld-review Review HLD for <project/service>
```

Output: `projects/<id>/reviews/ARC-<id>-HLDR-v1.0.md`

---

## Review Structure

| Section | Contents |
|---------|----------|
| Review Summary | Overall assessment and recommendation |
| Principles Alignment | How design aligns with each principle |
| Requirements Coverage | All requirements traceable to components |
| Risk Mitigation | How identified risks are addressed |
| Non-Functional Assessment | Performance, security, scalability |
| Integration Review | External system interactions |
| Technology Choices | Appropriateness of selected technologies |
| Governance Compliance | Standards and policy adherence (PSPF/ISM/Essential Eight, Privacy Act 1988 and APPs, DSS where applicable) |
| Findings & Recommendations | Issues categorized by severity |

---

## Review Categories

| Category | Focus | Examples |
|----------|-------|----------|
| Architecture | Structural soundness | Layering, separation of concerns |
| Principles | Governance alignment | Cloud-first, open standards |
| Requirements | Coverage completeness | Missing or misinterpreted requirements |
| Security | Security posture | Authentication, encryption, boundaries |
| Scalability | Growth capacity | Horizontal scaling, bottlenecks |
| Integration | External interactions | API design, data flows |

---

## Severity Levels

| Severity | Impact | Action Required |
|----------|--------|-----------------|
| Critical | Fundamental flaw | Must fix before approval |
| Major | Significant risk | Should fix before approval |
| Minor | Improvement opportunity | Fix in detailed design |
| Observation | Best practice | Consider for future |

---

## One-Page Workflow

| Phase | Key Activities | ArcKit Commands |
|-------|----------------|-----------------|
| Foundation | Define principles and requirements | `/arckit.principles`, `/arckit.requirements` |
| Risk | Identify and assess risks | `/arckit.risk` |
| Design | Create HLD | Manual or `/arckit.diagram` |
| Review | Review HLD against standards | `/arckit.hld-review` |
| Approval | Address findings, get sign-off | Manual |

---

## Review Checklist

- Every architecture principle has a design alignment statement.
- All requirements (BR, FR, NFR, INT) traceable to design elements.
- Identified risks have corresponding design mitigations.
- Security architecture addresses all NFR-SEC requirements.
- AU policy expectations are explicitly addressed where relevant: PSPF-aligned security governance, ACSC ISM and Essential Eight uplift, Privacy Act 1988 and APPs (including PIA expectations and NDB scheme readiness).
- Public-facing services: DSS criteria are considered and evidence is captured (or explicitly marked not applicable).
- Integration points have defined contracts and error handling.
- Technology choices align with standards and principles.
- No critical or major findings remain unaddressed.

---

## Principles Alignment Format

| Principle | Alignment | Evidence |
|-----------|-----------|----------|
| Cloud-First | Aligned | Uses managed cloud services (e.g., AWS/Azure/GCP PaaS) |
| Open Standards | Partial | REST APIs, but proprietary auth |
| Security by Design | Aligned | Defense in depth, zero trust |

---

## Key Principles

1. **Principles as Guardrails**: Design must demonstrably align with principles.
2. **Traceability**: Every component should trace to requirements.
3. **Risk Awareness**: Design should address identified risks.
4. **Early Feedback**: Review early to avoid costly rework.
5. **Constructive Critique**: Focus on improving the design, not blocking.
