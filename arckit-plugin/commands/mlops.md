---
description: "Create MLOps strategy with AU AI governance integration"
---

Generate an MLOps strategy that integrates AU AI governance requirements.

## User Input

```text
$ARGUMENTS
```

## Output

- `projects/{project-dir}/ARC-{PROJECT_ID}-MLOP-v1.0.md`

## Template

Read `.arckit/templates/mlops-template.md`.

## Required integration

Link MLOps operating model to these AI artifacts where applicable:
- `ARC-{PROJECT_ID}-AIGA-v*.md`
- `ARC-{PROJECT_ID}-AIIA-v*.md`
- `ARC-{PROJECT_ID}-AITS-v*.md`
- `ARC-{PROJECT_ID}-AIUR-v*.md`
- `ARC-{PROJECT_ID}-AIGC-v*.md`

## Minimum content

1. Model/data lifecycle and release controls.
2. Monitoring for drift, safety, transparency, security, and compliance.
3. Human oversight and intervention model.
4. Incident and re-validation workflow.
5. Decommissioning and records retention approach.

## AU policy alignment

- AI policy v2.0 (monitoring/re-validation obligations)
- AI technical standard (monitoring + incident + decommission criteria)
- OAIC guidance for privacy-impacting use cases
