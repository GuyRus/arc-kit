# AI Residual UK Scan (Default AI Paths)

Date: 2026-02-15 (AEDT)

## Scope

Scan target: **AI-scope default paths only** (templates, prompts, commands, guides, AI wiring touched in the AU rewrite).

- Scoped files: **45**
- Detection patterns: UK-in-AI-context patterns (e.g. `UK AI`, `UK JSP 936`, `Legacy UK`, `UK-modeled`)

## Result

- **Result:** ✅ PASS
- **Disallowed residual references:** **0**
- Total matched UK-context lines: 40
- Allowed exceptions: 40 (all justified)

## Allowed exception classes

1. **Legacy/deprecation markers**
   - Explicit stubs and archive pointers (e.g. `legacy-uk`, deprecated UK guides/titles).
2. **Defence source-gap declarations**
   - Required statement that no public AU Defence-wide equivalent to UK JSP 936 was identified.
3. **Anti-regression controls**
   - Prompt/command guardrails such as “Do not use UK AI policy constructs in default outputs.”
4. **Legacy compatibility metadata**
   - Manifest entries for deprecated legacy-UK surfaces.

## Artifacts

- Machine-readable report: `reviewer-pack/ai-residual-uk-scan.json`
- Raw line hits: `reviewer-pack/ai-residual-uk-scan.raw.txt`
