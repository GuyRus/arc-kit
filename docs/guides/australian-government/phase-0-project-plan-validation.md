# Phase 0 (Project Plan) — Validation Results

## Scope validated

- `.codex/prompts/arckit.plan.md`
- `arckit-plugin/commands/plan.md`
- `.arckit/templates/project-plan-template.md`
- `arckit-plugin/templates/project-plan-template.md`
- `docs/guides/plan.md`
- `arckit-plugin/docs/guides/plan.md`

## Checks run

### 1) Residual UK policy scan (targeted)

Command:

```bash
grep -RInE "UK Government|GDS|gov\.uk|GOV\.UK|NCSC|HM Treasury|Cabinet Office|Technology Code of Practice|TCoP|Digital Marketplace|G-Cloud|DOS Outcomes|DOS Specialists|UK GDPR|Data Protection Act 2018|DPA 2018|Cyber Essentials|Ministry of Defence|JSP 936|JSP 440|£" \
  .codex/prompts/arckit.plan.md \
  arckit-plugin/commands/plan.md \
  .arckit/templates/project-plan-template.md \
  arckit-plugin/templates/project-plan-template.md \
  docs/guides/plan.md \
  arckit-plugin/docs/guides/plan.md
```

Result: **0 matches**.

### 2) Core/plugin parity checks

Commands:

```bash
diff -u .codex/prompts/arckit.plan.md arckit-plugin/commands/plan.md
diff -u .arckit/templates/project-plan-template.md arckit-plugin/templates/project-plan-template.md
diff -u docs/guides/plan.md arckit-plugin/docs/guides/plan.md
```

Result: **no differences** (parity preserved).

## Quality assessment summary

- Original ArcKit project-plan structure retained (phases, gates, diagrams, activity tables).
- AU policy baseline now explicit in planning prompt/template/guide.
- Gate model and assurance framing moved to AU context.
- Procurement/privacy/security hooks re-anchored to AU references.
- No default UK policy language remains in phase-0 planning surfaces.

## Known limitations

- `SOURCE_GAP`: richer machine-readable extraction for some digital.gov.au toolkit pages should be added to policy corpus in a later pass.
- `SOURCE_GAP`: agency-specific assurance threshold nuances may need tailoring per deployment context.
