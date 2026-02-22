# Defence Secure by Design Assessment (AU)

`/arckit.mod-secure` generates a Defence Secure by Design assessment for Australian Defence contexts.

Because Defence assurance pathways and policy baselines are often organisation-specific, the output:

- preserves a useful Secure by Design assessment structure (executive summary, evidence index, findings, actions)
- avoids inventing Defence-specific policy details when not evidenced
- records explicit `SOURCE_GAP` items for policy owners to confirm

---

## Inputs

| Artefact | Purpose |
|----------|---------|
| Requirements (`ARC-<id>-REQ-v*.md`) | Security, resilience, identity, logging and data handling constraints |
| Architecture diagrams (`ARC-<id>-DIAG-*.md`) | Trust boundaries, deployment topology, data flows |
| Risk register (`ARC-<id>-RISK-v*.md`) | Security risks, treatments, residual risk acceptance |
| Civilian Secure by Design (`ARC-<id>-SECD-v*.md`) | Reuse applicable control evidence where relevant |
| ADRs (`ADR-*.md`) | Security-significant decisions and trade-offs |
| External evidence (`projects/<project>/external/*`) | Threat models, pen tests, audits, accreditation artefacts (if provided) |

---

## Command

```bash
/arckit.mod-secure Defence Secure by Design assessment for <system>
```

Output: `projects/<id>/ARC-<id>-SECD-MOD-vX.Y.md`

> **Auto-versioning**: re-running increments the version (minor for refreshed assessment; major for materially changed scope).

---

## What The Assessment Covers

- governance, assurance gates, and residual risk acceptance
- identity, access, and privileged administration (including operational constraints)
- classification handling and data protection (including crypto/key management expectations)
- secure engineering and supply chain controls (SBOM/provenance where appropriate)
- logging, monitoring, detection, and incident response readiness
- resilience and recovery (backup/restore, DR expectations)
- environment separation, hardening, patching, vulnerability management

---

## Useful Organising Lenses

These are optional structures used to check completeness and make reviews easier. They are not claimed as mandatory unless evidenced in your artefacts:

- Secure by Design principles (context, security-from-start, defence in depth, secure patterns, continuous risk management, supply chain, through-life assurance)
- NIST Cybersecurity Framework (Identify/Protect/Detect/Respond/Recover)
- Three Lines of Defence (delivery ownership, assurance/oversight, independent review)

---

## Recommended Deep-Dive Sections

For Beta/Live (and most higher-classification systems), expect deeper coverage of:

- vulnerability scanning and patch management (coverage, SLAs, exception process)
- third-party and supply chain risk (supplier access, assurance reports/attestations if provided, OSS controls)
- backup/restore/DR readiness (RTO/RPO, restore tests)
- secure SDLC and build integrity (SAST/DAST/SCA, secrets scanning, signing/provenance where appropriate)

---

## Security Classification (AU)

Use AU classification styles (example): `OFFICIAL:Sensitive`.

Common options used in templates:

- PUBLIC
- OFFICIAL
- OFFICIAL:Sensitive
- PROTECTED
- SECRET
- TOP SECRET
