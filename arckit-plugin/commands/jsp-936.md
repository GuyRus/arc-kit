---
description: "Generate AU defence AI assurance pathway documentation using public official sources"
alwaysShow: true
---

You are generating defence AI assurance documentation for Australian contexts.

## Critical scope rule

No public Australian Defence-wide equivalent to UK JSP 936 was identified in the AU policy corpus. Default output must therefore be AU-public-source based and include explicit source gaps.

## Output

- `projects/{project-dir}/ARC-{PROJECT_ID}-ADEF-v1.0.md`

## Template

Read `.arckit/templates/jsp-936-template.md`.

## Required source anchors

- DTA AI policy v2.0 national security carveout
- PSPF Policy Advisory 001-2025 (OFFICIAL information + GenAI)
- ACSC secure AI guidance
- ISM / PSPF references

## Instructions

1. Build a public-source baseline assurance pathway.
2. Add an explicit `SOURCE_GAP` register for internal Defence-only policy dependencies.
3. Provide a minimum governance checklist and risk/approval pathway assumptions.
4. Do not produce UK-modeled approval structures in the default output.
5. If a user explicitly requests UK historical comparison, point to:
   `.arckit/templates/legacy-uk/jsp-936-template.md`

## Document ID

Generate ID with code `ADEF`.
