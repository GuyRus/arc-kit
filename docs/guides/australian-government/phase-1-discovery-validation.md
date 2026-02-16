# Phase 1 (Discovery) — Validation Results

## Scope validated

- `.codex/prompts/arckit.principles.md`
- `arckit-plugin/commands/principles.md`
- `docs/guides/principles.md`
- `arckit-plugin/docs/guides/principles.md`
- `.codex/prompts/arckit.stakeholders.md`
- `arckit-plugin/commands/stakeholders.md`
- `docs/guides/stakeholders.md`
- `arckit-plugin/docs/guides/stakeholders.md`
- `.codex/prompts/arckit.risk.md`
- `arckit-plugin/commands/risk.md`
- `docs/guides/risk.md`
- `arckit-plugin/docs/guides/risk.md`
- `.codex/prompts/arckit.sobc.md`
- `arckit-plugin/commands/sobc.md`
- `docs/guides/sobc.md`
- `arckit-plugin/docs/guides/sobc.md`
- `.arckit/templates/{architecture-principles,stakeholder-drivers,risk-register,sobc}-template.md`
- `arckit-plugin/templates/{architecture-principles,stakeholder-drivers,risk-register,sobc}-template.md`

## Checks run

### 1) Residual UK policy scan (phase-1 files)

Result: **0 explicit UK-policy matches** for terms such as UK Government, GDS, GOV.UK, HM Treasury, Digital Marketplace/G-Cloud, NCSC, TCoP, UK-specific defence references, or GBP symbols.

### 2) Core/plugin parity

Prompt↔command, guide↔guide, and template↔template pairs were synchronized and validated.

## Quality summary

- Discovery command utility/structure retained.
- Risk and SOBC workflows remain comprehensive.
- Policy language now anchors to AU Commonwealth settings.
- Currency and compliance examples shifted to AU context.

## Known limitations

- `SOURCE_GAP`: exact approval thresholds and assurance escalation are agency-specific and must be tailored per deployment.
