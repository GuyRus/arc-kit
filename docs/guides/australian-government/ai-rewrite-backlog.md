# AU AI Rewrite Backlog (First-Principles)

Branch: `feat/au-ai-first-principles`  
Scope: **AI-specific ArcKit surfaces only** (templates, commands, prompts, guides, wiring)

## Guardrails

- Start from policy, not from existing UK wording.
- Every rewritten file must be read end-to-end before edits.
- Every substantive policy claim must map to a sourced AU policy paragraph/section.
- No shallow substitutions.
- UK material retained only under clearly-marked `legacy-uk` paths.

## Phase A — Inventory & Source Corpus

- [x] **AI-001** Build exhaustive AI file inventory (templates, commands, prompts, docs, wiring)
- [x] **AI-002** Build exhaustive UK policy inventory used by those files (with file/line citations)
- [x] **AI-003** Build AU counterpart policy universe (cross-agency): DTA, Finance, OAIC, PM&C, AGD, ASD/ACSC, Defence, ONDC, legislation.gov.au
- [x] **AI-004** Download official AU sources (PDF preferred, otherwise canonical HTML) into `docs/policy-sources/au/ai/`
- [x] **AI-005** Convert/downloaded sources to markdown/text and record provenance (URL, owner, accessed time AEDT, checksum)
- [x] **AI-006** Produce UK→AU mapping and gap analysis (replace / add / delete / no-equivalent)

## Phase B — Policy Requirements Extraction

- [x] **AI-007** Extract paragraph-level AU requirements relevant to AI governance artifacts
- [x] **AI-008** Build section-level traceability matrix for each target artifact:
  - AI governance assessment
  - AI use case register
  - AI transparency statement
  - AI impact assessment
  - AI governance checklist
  - Defence-specific AI assurance path
- [x] **AI-009** Define mandatory vs optional sections and minimum evidence rules per artifact

## Phase C — Rewrite (File-by-file)

- [x] **AI-010** Rewrite AI templates in `.arckit/templates/` from first principles
- [x] **AI-011** Mirror template rewrites to `arckit-plugin/templates/` (zero drift)
- [x] **AI-012** Rewrite commands: `ai-playbook`, `atrs`, `jsp-936`, `mlops` (and any AI-linked command surfaces)
- [x] **AI-013** Rewrite prompts: `.codex/prompts/arckit.ai-playbook.md`, `arckit.atrs.md`, `arckit.jsp-936.md`, `arckit.mlops.md`
- [x] **AI-014** Rewrite guides in `docs/guides/*` + plugin mirror
- [x] **AI-015** Update script/wiring for document IDs and command->template mapping
- [x] **AI-016** Move UK AI content to explicit legacy paths with deprecation markers

## Phase D — Validation & Demo

- [x] **AI-017** Run UK residual scan for AI scope only (default paths)
- [x] **AI-018** Enforce no UK references outside legacy paths (or document justified exception)
- [x] **AI-019** Run available validations/tests and record limitations
- [x] **AI-020** Generate AI-focused AU federal demo artifacts and verify traceability to source corpus
- [x] **AI-021** Prepare reviewer pack: changed files, mapping, traceability, known gaps

## Notes

This backlog is intentionally strict. Completion requires evidence, not just edited text.
