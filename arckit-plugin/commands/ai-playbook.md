---
description: "Generate AU AI governance assessment artifacts grounded in Australian Government policy"
---

You are helping an Australian Government team produce policy-grounded AI governance artifacts.

## User Input

```text
$ARGUMENTS
```

## Required outputs

Generate these files in `projects/{project-dir}/`:

1. `ARC-{PROJECT_ID}-AIGA-v1.0.md` (AU AI governance assessment)
2. `ARC-{PROJECT_ID}-AIUR-v1.0.md` (AU AI use case register)
3. `ARC-{PROJECT_ID}-AIGC-v1.0.md` (AU AI governance checklist)
4. If the use case is in-scope: `ARC-{PROJECT_ID}-AIIA-v1.0.md` (AU AI impact assessment)

## Policy baseline (must be used)

- Policy for the responsible use of AI in government 2.0
- Standard for accountability 2.0
- Standard for AI transparency statements 2.0
- Guidance for the AI impact assessment tool + AI impact assessment tool
- Australian Government AI technical standard
- OAIC AI/privacy guidance (as relevant)

## Instructions

1. Determine whether the use case is in-scope using Appendix C criteria.
2. Identify mandatory obligations by policy section:
   - strategy and oversight
   - preparedness and operations
   - AI use case impact assessment
3. Read and apply these templates:
   - `.arckit/templates/au-ai-governance-assessment-template.md`
   - `.arckit/templates/au-ai-use-case-register-template.md`
   - `.arckit/templates/au-ai-governance-checklist-template.md`
   - `.arckit/templates/au-ai-impact-assessment-template.md` (when in-scope)
4. Populate document control fields and create evidence-backed content.
5. Include explicit gaps as `SOURCE_GAP` or `TODO` where authoritative policy is unavailable.
6. Do not use UK AI policy constructs in default outputs.

## Document IDs

Use `.arckit/scripts/bash/generate-document-id.sh`:

- `AIGA` for governance assessment
- `AIUR` for use case register
- `AIGC` for governance checklist
- `AIIA` for impact assessment

## Minimum quality checks before completion

- Every mandatory policy requirement is marked Met/Partial/Not met with evidence.
- Register fields match Standard for accountability minimum fields.
- Risk and re-validation logic is consistent across AIGA/AIIA/AIUR.
- High-risk pathway actions are explicit (board/senior executive + DTA reporting).
