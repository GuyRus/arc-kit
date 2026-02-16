# Phase 6 (Procurement & Research) — UK to AU Policy Mapping

## Scope

Phase 6 covers procurement and market/data research surfaces:

- `dos`
- `gcloud-search`
- `gcloud-clarify`
- `datascout`
- `research`
- `aws-research`
- `azure-research`
- `gcp-research`

Updated across prompt/command pairs, guides, agent specs, and templates (core + plugin parity).

## Migration Intent

Retain ArcKit market discovery and procurement-analysis richness while replacing UK-default frameworks, portals, and compliance references with AU Commonwealth equivalents.

## Policy Mapping

| Previous UK-oriented concept | AU replacement used | Notes |
|---|---|---|
| Digital Marketplace, G-Cloud, DOS default channels | BuyICT / AusTender / CPR-compliant sourcing language | Keeps structured procurement outputs without UK lock-in |
| UK API/open-data defaults (`api.gov.uk`, `data.gov.uk`) | AU open-data defaults (`api.gov.au`, `data.gov.au`) | Preserves open-data-first research flow |
| UK regulator/compliance assumptions | Privacy Act 1988 (APPs), OAIC, ASD ACSC framing | Maintains compliance checks in scoring and recommendations |
| UK cloud region defaults (London/UK South/West) | Australian region defaults (Sydney/Melbourne/Canberra equivalents per provider) | Preserves region suitability logic |
| UK domain-specific dataset exemplars | AU public dataset exemplars (ABS, AIHW, BoM, AEMO, ABR/ASIC, etc.) | Keeps category depth while localizing authoritative starting points |

## AU Sources Used

| Source | Use in rewrite |
|---|---|
| Commonwealth Procurement Rules (CPRs) | Procurement route and evaluation framing |
| BuyICT and AusTender channels | Panel/marketplace equivalent procurement pathways |
| data.gov.au / api.gov.au | Open data and API discovery starting points |
| Privacy Act 1988 + APPs / OAIC | Privacy and data-handling checks in vendor/source evaluation |
| ASD ACSC / ISM / Essential Eight | Security/compliance considerations for cloud/vendor research |

## Source Gaps

- `SOURCE_GAP`: exact panel names and pathways vary by agency and over time.
- `SOURCE_GAP`: sovereign/protected cloud controls may require agency-specific interpretation beyond public provider guidance.

## Rewrite Character

- Existing research, scoring, and comparison structure retained.
- UK defaults removed from non-legacy paths in this phase scope.
- AU procurement and open-data context now drives default guidance.
