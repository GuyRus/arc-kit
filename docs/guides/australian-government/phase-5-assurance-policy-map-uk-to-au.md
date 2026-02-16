# Phase 5 (Assurance) — UK to AU Policy Mapping

## Scope

Phase 5 covers assurance and security command surfaces:

- `adr`
- `dpia`
- `secure`
- `mod-secure`
- `service-assessment`
- `tcop`

Updated across prompt/command pairs, guides, and templates (core + plugin parity).

## Migration Intent

Preserve ArcKit assurance depth and structure while replacing UK-default governance, security, service assurance, and privacy references with Australian Commonwealth equivalents.

## Policy Mapping

| Previous UK-oriented concept | AU replacement used | Notes |
|---|---|---|
| GDS Service Standard and GDS assessments | Digital Service Standard (DSS) assurance framing | Keeps 14-point assurance structure intent and evidence workflow |
| Technology Code of Practice (TCoP) | Digital Experience Policy + DSS | Preserves compliance assessment shape and point-by-point analysis |
| NCSC CAF/Cyber Essentials | ASD ACSC + ISM/Essential Eight | Keeps secure-by-design controls and maturity expectations |
| UK GDPR / DPA 2018 / ICO | Privacy Act 1988 (APPs) + OAIC | Maintains privacy-by-design and regulator escalation logic |
| UK service manual / gov.uk links | DTA/Digital.gov.au and AU policy references | Removes UK-default source dependency |
| UK MOD references in default defence workflow | Australian Department of Defence context | Preserves defence-specific security workflow without UK defaulting |

## AU Sources Used

| Source | Use in rewrite |
|---|---|
| Digital Service Standard (DTA) | Service assessment and ADR assurance integration |
| Digital Experience Policy | DX policy review point mapping (former TCoP flow) |
| PSPF / ISM / Essential Eight (ASD ACSC) | Secure-by-design and cyber control assessment |
| Privacy Act 1988 + APPs / OAIC guidance | DPIA, breach/notification, and privacy governance framing |
| Defence public policy context | Defence secure-by-design alignment where applicable |

## Source Gaps

- `SOURCE_GAP`: agency-specific Defence security baselines and accreditation references vary and must be localized.
- `SOURCE_GAP`: some AU assurance links are consolidated to policy landing pages where direct one-to-one UK equivalents do not exist.

## Rewrite Character

- Existing command/template structure retained.
- UK defaults removed from non-legacy paths in this phase scope.
- AU governance language integrated while preserving assessor utility and evidence richness.
