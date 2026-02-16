# Phase 0 (Project Plan) — UK to AU Policy Mapping

## Scope

This phase covers project planning surfaces:

- `.codex/prompts/arckit.plan.md`
- `arckit-plugin/commands/plan.md`
- `.arckit/templates/project-plan-template.md`
- `arckit-plugin/templates/project-plan-template.md`
- `docs/guides/plan.md`
- `arckit-plugin/docs/guides/plan.md`

## Migration Intent

Replace UK-default project governance framing with AU Commonwealth policy-grounded planning, while preserving practical delivery usability.

## Policy Mapping (Planning Domain)

| Previous UK-oriented concept | AU replacement used in Phase 0 | Notes |
|---|---|---|
| GDS default framing | Digital Experience Policy + Digital Service Standard | AU whole-of-government service quality baseline |
| UK assessment gate wording | Finance Assurance Reviews / Gateway / IRA style assurance cadence | Used as AU assurance backbone where applicable |
| UK procurement framing | Commonwealth Procurement Rules (CPRs) | Value-for-money and procurement governance alignment |
| UK privacy references (GDPR/DPA) | Privacy Act 1988 + APPs | AU privacy baseline for planning and controls |
| UK security references | PSPF + ASD ISM | AU security baseline for service planning |

## AU Sources Used

| Source | URL / artifact | Use in rewrite |
|---|---|---|
| Digital Service Standard | https://www.digital.gov.au/policy/digital-experience/digital-service-standard | Planning quality criteria and service delivery framing |
| Digital Experience Policy | https://www.digital.gov.au/policy/digital-experience/digital-experience-policy | Policy compliance framing for digital services |
| Assurance Reviews Process Overview | https://www.finance.gov.au/government/assurance-reviews-and-risk-assessment/assurance-reviews-process-overview | Gate and assurance cadence framing |
| Gateway Reviews Process | https://www.finance.gov.au/government/assurance-reviews-and-risk-assessment/gateway-reviews-process | High-risk proposal checkpoint model |
| Commonwealth Procurement Rules | https://www.finance.gov.au/government/procurement/commonwealth-procurement-rules | Procurement and value-for-money constraints |
| PSPF | https://www.protectivesecurity.gov.au | Security policy baseline |
| Existing local corpus (Privacy/PSPF/Finance guidance) | `docs/policy-sources/au/ai/converted/*` | Supplemental AU policy context already in-repo |

## Source Gaps

- `SOURCE_GAP`: detailed, machine-readable extraction of the Digital Experience Toolkit “service design and delivery process” page was not available via static fetch at rewrite time; lifecycle wording is kept general and non-fabricated.
- `SOURCE_GAP`: exact mandatory use thresholds for each assurance pattern in non-major proposals can vary by agency/program context; template uses applicability and tailoring fields rather than hard-coded absolute triggers.

## Rewrite Characteristics

This phase keeps the original ArcKit project-plan structure (phases, gates, diagrams, and activity tables) and rewires policy alignment to AU settings:

- Step/section structure preserved so existing ArcKit utility is retained
- UK policy anchors replaced with AU policy families and AU assurance framing
- budgeting and governance defaults changed to AU context (AUD, OFFICIAL default guidance)
- privacy/security/procurement hooks embedded as phase controls
- explicit source traceability section added to template

## Residual UK Policy Rule

Project plan surfaces should contain **no default UK policy references** unless explicitly tagged as legacy context.
