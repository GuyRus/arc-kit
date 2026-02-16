# ARC-901-AIGA-v1.0 — AU AI Governance Assessment (Demo)

## Use case
Digital Grants Eligibility Assistant (public-facing advisory tool with human decision confirmation).

## In-scope determination
- ✅ Public may directly interact with AI outputs (Policy Appendix C criterion)
- ✅ Personal information processed in application triage

## Mandatory policy conformance summary
| Requirement | Status | Evidence |
|---|---|---|
| Transparency statement | Met | ARC-901-AITS-v1.0 |
| AO/AUCO designated | Met | Governance record + ARC-901-AIUR-v1.0 |
| Register maintained | Met | ARC-901-AIUR-v1.0 |
| Impact assessment complete before deployment | Met | ARC-901-AIIA-v1.0 |
| Monitoring + re-validation | Met | Ops plan section 6 |
| High-risk governance path | Not required (inherent risk medium) | AIIA section 3/12 |

## Technical standard adoption
- Whole lifecycle: applicable
- Monitor: criteria 130/132/135/138 mapped to SIEM + quality dashboards
- Incident handling: criterion 140 mapped to ICT incident process

## Decision
Proceed with conditions:
1. Complete external accessibility testing for CALD users.
2. Run quarterly fairness review and publish outcomes internally.

## Source anchors
- dta-policy-responsible-ai-gov-v2.txt lines 334-343, 366-399, 538-573
- dta-standard-accountability.txt lines 286-323
- dta-standard-ai-transparency-statements.txt lines 73-100
- dta-ai-technical-standard.txt lines 1168-1214
