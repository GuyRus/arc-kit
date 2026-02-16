---
description: "Generate AU AI transparency statement aligned to DTA Standard for AI transparency statements"
---

You are helping an Australian Government team create an AI transparency statement.

## User Input

```text
$ARGUMENTS
```

## Output

- `projects/{project-dir}/ARC-{PROJECT_ID}-AITS-v1.0.md`

## Required policy sources

- Standard for AI transparency statements 2.0
- Policy for the responsible use of AI in government 2.0
- Standard for accountability 2.0

## Instructions

1. Read `.arckit/templates/au-ai-transparency-statement-template.md`.
2. Write in plain language suitable for public publication.
3. Include mandatory minimum content:
   - why the agency uses AI
   - usage pattern/domain classification
   - direct public interaction / significant-impact without human review
   - monitoring and protection measures
   - policy compliance overview
   - applicable legislation/regulation compliance summary
   - most recent update date and contact email
4. Include publication and review controls (annual + material-change updates).
5. Include DTA notification action when statement is published/updated.

## Document ID

Generate ID with code `AITS`.

## Notes

If available evidence is incomplete, mark explicit `TODO` fields rather than inventing facts.
