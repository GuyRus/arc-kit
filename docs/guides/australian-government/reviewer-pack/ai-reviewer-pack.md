# AI Reviewer Pack (Finalisation Pass)

Branch: `feat/au-ai-first-principles`  
Baseline before this pass: `868355d`

## Purpose of this pass

Finalise AI rewrite evidence after prior reporting overflow, without redoing major rewrites. This pass focused on:

1. Auditing AI backlog items **AI-007..AI-021** against repository evidence.
2. Filling only targeted gaps (policy reference explicitness + refreshed validation artifacts).
3. Publishing a concise reviewer-ready evidence set.

## Targeted changes made in this pass

### 1) Explicit policy references strengthened (minimal edits)

- Updated:
  - `.arckit/templates/au-ai-impact-assessment-template.md`
  - `arckit-plugin/templates/au-ai-impact-assessment-template.md`
- Change: added **Policy baseline references** block explicitly naming:
  - Policy for the responsible use of AI in government 2.0
  - Guidance for the AI impact assessment tool (PDF)
  - Australian Government AI technical standard

### 2) Traceability anchor explicitness improved

- Updated:
  - `docs/guides/australian-government/ai-template-traceability-matrix.md`
- Change: added canonical source anchor section with converted corpus file paths for the same three DTA sources.

### 3) Reviewer evidence regenerated

- Added:
  - `docs/guides/australian-government/ai-validation-results.md`
  - `docs/guides/australian-government/ai-residual-uk-scan.md`
  - `docs/guides/australian-government/ai-template-depth-report.md`
- Refreshed machine-readable artifacts in `docs/guides/australian-government/reviewer-pack/`:
  - `ai-residual-uk-scan.json`
  - `ai-residual-uk-scan.raw.txt`
  - `ai-template-parity-report.json`
  - `ai-template-depth-report.json`
  - `check-bash-n.raw.txt`
  - `check-python-compile.raw.txt`
  - `check-manifest-json.raw.txt`
  - `check-pytest.raw.txt`

## AI-007..AI-021 audit status

| Backlog item | Status | Evidence |
|---|---|---|
| AI-007 AU paragraph-level requirements extraction | ✅ Complete | `ai-au-requirements-extraction.md` |
| AI-008 section-level traceability matrix | ✅ Complete | `ai-template-traceability-matrix.md` |
| AI-009 mandatory/optional section rules + evidence minima | ✅ Complete | `ai-template-section-rules.md` |
| AI-010 rewrite AI templates in `.arckit/templates` | ✅ Complete | AU templates + `jsp-936-template.md`, `mlops-template.md` |
| AI-011 mirror template rewrites to plugin (zero drift) | ✅ Complete | `ai-template-parity-report.json` (0 mismatches) |
| AI-012 rewrite AI-linked commands | ✅ Complete | `arckit-plugin/commands/{ai-playbook,atrs,jsp-936,mlops}.md` |
| AI-013 rewrite AI-linked prompts | ✅ Complete | `.codex/prompts/arckit.{ai-playbook,atrs,jsp-936,mlops}.md` |
| AI-014 rewrite guides + plugin mirror | ✅ Complete | `docs/guides/{ai-playbook,atrs,jsp-936,mlops}.md` + plugin mirror |
| AI-015 update wiring/mappings/doc IDs | ✅ Complete | `scripts/bash/{generate-document-id,migrate-filenames,create-project}.sh`, `docs/manifest.json`, `src/arckit_cli/__init__.py` |
| AI-016 move UK AI content to explicit legacy paths with deprecation markers | ✅ Complete | `.arckit/templates/legacy-uk/*`, `docs/guides/uk-government/*` |
| AI-017 run residual UK scan (AI-scope default paths) | ✅ Complete | `ai-residual-uk-scan.md` + JSON/raw |
| AI-018 enforce no UK refs outside allowed legacy/source-gap cases | ✅ Complete | Residual scan disallowed count = 0 |
| AI-019 run available validations/tests + record limitations | ✅ Complete | `ai-validation-results.md` |
| AI-020 generate AU federal demo artifacts + traceability | ✅ Complete | `reviewer-pack/demo-artifacts/ARC-901-*.md` |
| AI-021 prepare reviewer pack | ✅ Complete | This file + linked evidence docs |

## File map (review order)

1. `ai-reviewer-pack.md` (this summary)
2. `ai-validation-results.md`
3. `ai-residual-uk-scan.md`
4. `ai-template-depth-report.md`
5. Core extraction/traceability/rules:
   - `ai-au-requirements-extraction.md`
   - `ai-template-traceability-matrix.md`
   - `ai-template-section-rules.md`
6. Machine outputs/logs in `reviewer-pack/`

## Remaining known gaps

Unchanged from prior phase and explicitly documented:

1. No public Defence-wide equivalent to UK JSP 936 (managed via `SOURCE_GAP` process).
2. BuyICT page static extraction limitation (JS-rendered content).
3. `pytest` unavailable in current execution environment.
