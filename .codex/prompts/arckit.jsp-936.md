---
description: "Generate AU defence AI assurance pathway documentation using public official sources"
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

1. Build a public-source baseline assurance pathway that stays useful as a generic assurance pack.
2. Add an explicit `SOURCE_GAP` register for internal Defence-only policy dependencies (risk taxonomy, approval chain, incident doctrine, ethical review processes).
3. Read available ArcKit artefacts (if present) and ground the pathway in evidence:
   - `ARC-*-REQ-*.md` (requirements)
   - `ARC-*-DATA-*.md` (data model)
   - `ARC-*-RISK-*.md` (risk register)
   - `ARC-*-SECD-*.md` (secure by design, if any)
   - `ARC-*-PIA-*.md` (privacy impact assessment, if any)
   - `ARC-*-DIAG-*.md` (architecture diagrams, if any)
   - `ADR-*.md` (decision records, if any)
4. Provide a through-life assurance lifecycle plan (gates, evidence, exit criteria) and a minimum evidence checklist.
5. Do not produce UK-modeled approval structures in the default output (no UK ministerial/TLB pathways).
6. If a user explicitly requests UK historical comparison, point to:
   - `.arckit/templates/legacy-uk/jsp-936-template.md`

## Document ID

Generate ID with code `ADEF`.
