# Phase 3 (Beta) — UK to AU Policy Mapping

## Scope

Phase 3 covers build/readiness command surfaces and templates:

- `sow`
- `evaluate`
- `hld-review`
- `dld-review`
- `backlog`
- `trello`
- `diagram`

Updated across prompt/command pairs, guides, and supporting templates.

## Migration Intent

Keep ArcKit Beta implementation and assurance workflow intact, while replacing UK-default procurement/compliance language with AU equivalents.

## Policy Mapping

| Previous UK-oriented concept | AU replacement used | Notes |
|---|---|---|
| UK procurement channels (Digital Marketplace/G-Cloud/DOS) | BuyICT/panel sourcing + CPR-compliant procurement wording | Preserves sourcing workflow structure |
| TCoP/GDS compliance callouts | DX Policy + Digital Service Standard callouts | Keeps governance gates and review depth |
| GDPR-centric compliance examples | Privacy Act 1988 + APP examples | Maintains compliance intent in AU legal context |
| GOV.UK reuse references | Generic reusable government services references | Retains reuse-by-default design logic |
| UK residency/currency defaults | Australian residency / AUD defaults | Localises implementation planning details |

## AU Sources Used

| Source | Use in rewrite |
|---|---|
| Commonwealth Procurement Rules (CPRs) | SOW/evaluation procurement framing |
| Digital Experience Policy + Digital Service Standard | Architecture/diagram/review compliance framing |
| Privacy Act 1988 + APP context | Security/privacy acceptance criteria and controls |
| PSPF/ISM context | Review and readiness security controls |

## Source Gaps

- `SOURCE_GAP`: panel/procurement channel names may differ by agency and contract environment.
- `SOURCE_GAP`: architecture compliance evidence templates should be tailored to agency assurance boards.

## Rewrite Character

- Beta command structures and sections preserved.
- UK references removed from default paths.
- AU policy language integrated without reducing planning/review utility.
