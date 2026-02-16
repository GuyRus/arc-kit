# AU AI Policy Corpus

Scope: Australian Government AI policy corpus used for ArcKit AI-first-principles rewrite.

## Layout

- `originals/` — downloaded canonical source documents
- `converted/` — extracted text/markdown used in drafting and traceability
- `provenance/` — source metadata JSON (canonical URL, retrieved URL, checksum, accessedAt AEDT, notes)
- `corpus-manifest.json` — corpus-level index

## Minimum source quality rules

- Prefer official PDF publications where available.
- If PDF is not available, use canonical government HTML/DOCX.
- Every source must have provenance metadata and checksum.
- Any unresolved source issues must be tracked in gap-analysis docs as `SOURCE_GAP`.

## Current approach

This corpus is committed using a selective-binary model (see `docs/policy-sources/README.md`).
