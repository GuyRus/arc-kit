# Policy Sources Governance

This directory stores policy-source material used to derive ArcKit governance content.

## Repository policy (AU AI phase)

We keep policy sources in three parallel forms for auditability:

- `originals/` — canonical downloaded source files (PDF/HTML/DOCX where published)
- `converted/` — extracted markdown/text used for analysis and drafting
- `provenance/` — per-source metadata (URL, owner, access time, checksum, format, conversion notes)

## What must be committed

Always commit:

1. Converted text (`converted/`)
2. Provenance metadata (`provenance/`)
3. Corpus manifests/indexes/mapping docs
4. Collection scripts

## Binary originals strategy

We use a **selective-binary** strategy:

- Keep original files that are directly cited by templates/prompts/reviewer packs.
- Avoid adding duplicate mirrors of the same source in multiple formats unless required.
- If source binaries become too large for practical repo use, migrate oversized sets to LFS or external artifact storage while preserving checksums + canonical URLs in provenance.

## Freshness and reproducibility expectations

- Each source must include a checksum and access timestamp.
- Major policy rewrites should refresh source captures and re-verify canonical URLs.
- If a source cannot be fetched cleanly (e.g., JS-rendered page), record it explicitly as a `SOURCE_GAP` with workaround notes.
