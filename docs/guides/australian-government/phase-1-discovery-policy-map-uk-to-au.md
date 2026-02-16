# Phase 1 (Discovery) — UK to AU Policy Mapping

## Scope

Phase 1 covers Discovery-governance command surfaces and templates:

- `principles`
- `stakeholders`
- `risk`
- `sobc`

Files updated include prompt/command pairs, guides, and core/plugin templates.

## Migration Intent

Keep ArcKit Discovery structure and workflow intact, while replacing UK-default governance and policy framing with AU Commonwealth equivalents.

## Policy Mapping

| Previous UK-oriented concept | AU replacement used | Notes |
|---|---|---|
| GDS service assessment framing | Digital Service Standard + DX Policy framing | Maintains service quality gate intent with AU policy anchors |
| HM Treasury Orange Book risk framing | Commonwealth Risk Management Policy / Finance risk guidance / ISO 31000-aligned language | Retains risk-register method while removing UK policy dependency |
| HM Treasury Green Book SOBC framing | AU Commonwealth investment/business case framing (5-case style retained for usability) | Preserves SOBC utility but aligns oversight language |
| UK procurement references (Digital Marketplace/G-Cloud/DOS) | CPR-compliant sourcing, BuyICT/panel-sourcing language | Maintains procurement planning function |
| UK privacy/security references | Privacy Act 1988 + APPs, PSPF/ISM/ASD/ACSC references | Aligns compliance planning to AU baseline |
| GBP examples | AUD examples | Currency/local context alignment |

## AU Sources Used

| Source | Use in rewrite |
|---|---|
| Digital Experience Policy + Digital Service Standard (digital.gov.au) | Discovery service quality and assessment framing |
| Finance assurance and risk guidance context | Risk governance wording updates |
| Commonwealth Procurement Rules (Finance) | SOBC sourcing and procurement language |
| Privacy Act 1988 + APP context | Compliance and data governance language |
| PSPF + ISM context | Security governance language |

## Source Gaps

- `SOURCE_GAP`: agency-specific approval thresholds vary by portfolio/program context and are not hard-coded.
- `SOURCE_GAP`: where SOBC workflows in agencies diverge from a 5-case style, local tailoring is required.

## Rewrite Character

- ArcKit structure retained (sections, gates, examples, command flow).
- UK policy and governance anchors replaced with AU policy anchors.
- No default UK policy references remain in phase-1 surfaces.
