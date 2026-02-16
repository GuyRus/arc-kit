# AI Validation Results (Finalisation Pass)

Date: 2026-02-15 (AEDT)

## Checks executed

| Check | Command / Method | Result | Evidence |
|---|---|---|---|
| Shell syntax | `bash -n scripts/bash/*.sh arckit-plugin/scripts/bash/*.sh` | ✅ PASS | `reviewer-pack/check-bash-n.raw.txt` |
| Python syntax/compile smoke | In-memory `compile()` over `scripts/converter.py`, `src/arckit_cli/__init__.py` | ✅ PASS (2 files) | `reviewer-pack/check-python-compile.raw.txt` |
| Manifest JSON parse | Python `json.loads` over `docs/manifest.json` | ✅ PASS | `reviewer-pack/check-manifest-json.raw.txt` |
| AI residual UK scan (default AI scope paths) | Pattern scan + allowlist classification | ✅ PASS (`disallowedCount: 0`) | `ai-residual-uk-scan.md`, `reviewer-pack/ai-residual-uk-scan.json` |
| Template parity (`.arckit/templates` vs `arckit-plugin/templates`) | SHA-256 per mirrored relative path | ✅ PASS (`mismatchCount: 0`, `pairCount: 54`) | `reviewer-pack/ai-template-parity-report.json` |
| Template depth vs AI-009 rules | Section presence + section word counts + req coverage check | ✅ PASS | `ai-template-depth-report.md`, `reviewer-pack/ai-template-depth-report.json` |
| Pytest suite | `python3 -m pytest -q` | ⚠️ NOT RUN (`No module named pytest`) | `reviewer-pack/check-pytest.raw.txt` |

## Outcomes

- Validation gates required for AI finalisation were run and passed where tooling was available.
- AI residual UK scan is clean for **disallowed** references in default AI paths.
- Template mirrors are in parity after targeted edits.
- Rule/section coverage is complete against AI-009 definitions.

## Limitations

1. Runtime/unit tests were not executed due missing `pytest` in environment.
2. Validation scope here is repository/static checks (not deployment/runtime behavioural testing).
