# AI Inventory Summary (AI-001 + AI-002)

Date: 2026-02-15  
Branch: `feat/au-ai-first-principles`

## Scope totals

- **AI-scope files inventoried:** 37
- **Unique file contents:** 24
- **Mirrored/duplicated files:** 26 files across 13 duplicate groups
- **Total lines in scope:** 21,444

### Surface breakdown

- Templates: 8 (4 primary + 4 plugin mirrors)
- Prompt/command surfaces: 8 (4 Codex prompts + 4 plugin command mirrors)
- Guides/docs: 12 (6 primary + 6 plugin mirrors)
- Wiring/scripts: 6 (3 primary + 3 plugin mirrors)
- Registry/help wiring: 2 (`docs/manifest.json`, `src/arckit_cli/__init__.py`)
- AU backlog control: 1

## UK policy/concept totals

- **Distinct UK policy/concept items identified:** 29
- **Initial dispositions:**
  - **replace:** 21
  - **retain-as-legacy:** 5
  - **delete:** 3

## Highest-density UK coupling hotspots

1. `.codex/prompts/arckit.jsp-936.md` (mirrored by `arckit-plugin/commands/jsp-936.md`) — deepest concentration of UK defence governance (JSP 936/JSP 440, RAISO, JROC/2PUS/TLB pathways).
2. `.codex/prompts/arckit.aits.md` (mirrored by `arckit-plugin/commands/aits.md`) — heavy UK ATRS/GOV.UK/DSIT/UK legal and publication requirements (now removed/renamed in AU scope).
3. `.arckit/templates/jsp-936-template.md` (+ plugin mirror) — UK defence assurance structure embedded in template skeleton.
4. `.arckit/templates/uk-gov-atrs-template.md` (+ plugin mirror) — UK legal/compliance and publication scaffolding is explicit.
5. `docs/manifest.json` + `src/arckit_cli/__init__.py` — UK categories/labels and compliance command wiring exposed in docs/help surfaces.

## Key problem areas for AU-first rewrite

- **Policy framework lock-in:** AI Playbook/AITS/JSP-936 are primary organising structures, not just references.
- **Defence approval model lock-in:** RAISO + 2PUS/JROC/TLB pathways are deeply hardcoded in JSP-936 surfaces.
- **Legal stack mismatch:** UK GDPR/DPA 2018/Equality/HRA/FOIA/ICO assumptions are distributed across templates and prompts.
- **Operational duplication risk:** mirror pairs double rewrite effort and drift risk unless changed in lockstep.
- **Wiring leakage:** UK terms persist in filename migration, project bootstrap messaging, docs manifest taxonomy, and CLI help text.
