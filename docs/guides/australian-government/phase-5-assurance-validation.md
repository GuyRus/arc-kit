# Phase 5 (Assurance) — Validation Results

## Scope validated

- `.codex/prompts/arckit.{adr,dpia,secure,mod-secure,service-assessment,tcop}.md`
- `arckit-plugin/commands/{adr,dpia,secure,mod-secure,service-assessment,tcop}.md`
- `docs/guides/{adr,dpia,secure,service-assessment,tcop}.md`
- `arckit-plugin/docs/guides/{adr,dpia,secure,service-assessment,tcop}.md`
- `.arckit/templates/{adr-template,dpia-template,mod-secure-by-design-template,service-assessment-prep-template,tcop-review-template,ukgov-secure-by-design-template}.md`
- `arckit-plugin/templates/{adr-template,dpia-template,mod-secure-by-design-template,service-assessment-prep-template,tcop-review-template,ukgov-secure-by-design-template}.md`

## Checks run

### 1) Residual UK policy scan (phase-5 files)

Command pattern included UK default markers (`UK Government`, `GDS`, `GOV.UK`, `TCoP`, `NCSC`, `Cyber Essentials`, `UK GDPR`, etc.) across all phase-5 files.

Result: **0 matches**.

### 2) Core/plugin parity

Prompt↔command and template↔template paired files were updated in lockstep.
Guide↔guide parity retained (`docs/guides` and `arckit-plugin/docs/guides`).

## Quality summary

- Assurance/security workflow depth preserved.
- AU policy and regulator framing now default for this scope.
- Defence and civilian secure-by-design paths remain distinct and usable.

## Known limitations

- `SOURCE_GAP`: agency-level assurance portals and Defence accreditation artefacts remain organization-specific and should be tailored locally.
