# AI-001 — AI File Inventory (AU rewrite scope)

Branch: `feat/au-ai-first-principles`  
Date: 2026-02-15  
Scope basis: `docs/guides/australian-government/ai-rewrite-backlog.md` (AI-only surfaces)

## Inventory method

- Enumerated AI-targeted surfaces from templates, prompts/commands, guides, plugin mirrors, and wiring/registry files.
- Read source files end-to-end for inventory correctness (including long-form JSP-936 prompt/command surfaces).
- Verified mirror drift with content hashing/diff where applicable.

## File counts

- **Total scoped files:** 37
- **Unique file contents:** 24
- **Mirrored/duplicate file groups:** 13 (26 files)

---

## 1) Templates (primary)

1. `.arckit/templates/uk-gov-ai-playbook-template.md`
2. `.arckit/templates/uk-gov-atrs-template.md`
3. `.arckit/templates/jsp-936-template.md`
4. `.arckit/templates/mlops-template.md`

## 2) Templates (plugin mirrors)

1. `arckit-plugin/templates/uk-gov-ai-playbook-template.md`
2. `arckit-plugin/templates/uk-gov-atrs-template.md`
3. `arckit-plugin/templates/jsp-936-template.md`
4. `arckit-plugin/templates/mlops-template.md`

## 3) Prompt surfaces (Codex)

1. `.codex/prompts/arckit.ai-playbook.md`
2. `.codex/prompts/arckit.aits.md`
3. `.codex/prompts/arckit.jsp-936.md`
4. `.codex/prompts/arckit.mlops.md`

## 4) Command surfaces (plugin)

1. `arckit-plugin/commands/ai-playbook.md`
2. `arckit-plugin/commands/aits.md`
3. `arckit-plugin/commands/jsp-936.md`
4. `arckit-plugin/commands/mlops.md`

## 5) Guides/docs (primary)

1. `docs/guides/ai-playbook.md`
2. `docs/guides/aits.md`
3. `docs/guides/jsp-936.md`
4. `docs/guides/mlops.md`
5. `docs/guides/uk-government/ai-playbook.md`
6. `docs/guides/uk-government/algorithmic-transparency.md`

## 6) Guides/docs (plugin mirrors)

1. `arckit-plugin/docs/guides/ai-playbook.md`
2. `arckit-plugin/docs/guides/aits.md`
3. `arckit-plugin/docs/guides/jsp-936.md`
4. `arckit-plugin/docs/guides/mlops.md`
5. `arckit-plugin/docs/guides/uk-government/ai-playbook.md`
6. `arckit-plugin/docs/guides/uk-government/algorithmic-transparency.md`

## 7) Wiring/scripts (primary)

1. `scripts/bash/generate-document-id.sh`
2. `scripts/bash/migrate-filenames.sh`
3. `scripts/bash/create-project.sh`

## 8) Wiring/scripts (plugin mirrors)

1. `arckit-plugin/scripts/bash/generate-document-id.sh`
2. `arckit-plugin/scripts/bash/migrate-filenames.sh`
3. `arckit-plugin/scripts/bash/create-project.sh`

## 9) Registry/index/help wiring

1. `docs/manifest.json` (docs categorisation/index wiring for AI artifacts)
2. `src/arckit_cli/__init__.py` (CLI help surfacing AI compliance commands)

## 10) AU backlog control file

1. `docs/guides/australian-government/ai-rewrite-backlog.md`

---

## Mirror/drift notes

- **Exact content mirrors** (same bytes): template pairs, guide pairs, script pairs listed above.
- **Near mirrors with path/runtime substitutions**: `.codex/prompts/arckit.{ai-playbook,aits,jsp-936,mlops}.md` vs `arckit-plugin/commands/{...}.md`.
- Implication: AU rewrite must be applied in paired surfaces to avoid ongoing drift.
