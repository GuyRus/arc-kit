# Digital Service Standard (DSS) Assurance Prep Guide

`/arckit.service-assessment` packages evidence for an Australian Government Digital Service Standard (DSS) assurance review. It produces an evidence map, RAG ratings, gaps, and an action plan.

The generated report includes **stage-specific expectations** (Discovery/Alpha/Beta/Live) for each DSS criterion so teams can see what “ready” means for their current stage and what evidence is missing.

---

## Command

```bash
/arckit.service-assessment STAGE=<discovery|alpha|beta|live> DATE=<YYYY-MM-DD optional>
```

Output: `projects/<id>/ARC-<id>-SVCASS-v1.0.md`.

---

## DSS Criteria (10)

1. Have clear intent
2. Know your user
3. Leave no one behind
4. Connect services
5. Build trust in design
6. Don’t reinvent the wheel
7. Do no harm
8. Innovate with purpose
9. Monitor your service
10. Keep it relevant

---

## Evidence Mapping (Summary)

| DSS focus | ArcKit sources | Notes |
|----------|----------------|------|
| Intent + value | Stakeholders, SOBC, requirements | Ensure success definition and value-for-money narrative are explicit |
| Users + inclusion | Stakeholders, research, requirements, service design | Accessibility and inclusion must be testable and evidenced |
| Trust, safety, privacy | `/arckit.secure`, `/arckit.pia`, risks, data model | Tie controls and mitigations to requirements and designs |
| Service ecosystem + reuse | Diagrams, integrations (INT), research, principles | Show “connect services” and “don’t reinvent” decisions |
| Measurement + relevance | SOBC metrics, operational readiness, ServiceNow design, monitoring approach | Define measurable outcomes and how they’re monitored |

---

## Prep Checklist

- Evidence heatmap reviewed; gaps assigned owners.
- A short show-and-tell deck created (use the prep document summary).
- Accessibility evidence ready (test reports, audit notes, WCAG mapping).
- Security and privacy evidence ready (secure-by-design, PIA, risk register, incident readiness).
- Measurement plan ready (KPIs, baselines, reporting cadence).
- Dry run scheduled; presenters and Q&A roles agreed.

---

## Assurance Review Tips

- Use real artefacts (repo links, screenshots, dashboards), not talking points.
- Keep the walkthrough short; spend most time on gaps and risk.
- Capture actions live and add to backlog within 24 hours.
- Re-run `/arckit.service-assessment` after fixes to demonstrate improvement.
