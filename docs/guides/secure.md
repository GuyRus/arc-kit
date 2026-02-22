# Secure by Design Assessment (AU)

`/arckit.secure` generates a Secure by Design assessment for Australian Government (civilian) projects.

It keeps the useful “assurance pack” structure (executive summary, evidence index, findings, actions) while aligning content to Australian Government expectations first:

- ASD Essential Eight maturity
- agency policy expectations aligned to PSPF/ISM (without inventing control IDs)
- cloud security and IRAP readiness where required
- Privacy Act 1988 (APPs) and Notifiable Data Breaches (NDB) readiness where personal information is in scope

---

## Inputs

| Artefact | Purpose |
|----------|---------|
| Requirements (`ARC-<id>-REQ-v*.md`) | Security, availability, resilience, logging and data constraints |
| Architecture diagrams (`ARC-<id>-DIAG-*.md`) | Trust boundaries, deployment topology, data flows |
| Risk register (`ARC-<id>-RISK-v*.md`) | Security and privacy risks, treatments and residual risk |
| PIA (`ARC-<id>-PIA-v*.md`) | APP risks, mitigations, data sharing constraints |
| ADRs (`ADR-*.md`) | Security-significant decisions and accepted trade-offs |
| External reports (`projects/<project>/external/*`) | Pen test reports, vulnerability scans, audits, threat models |

---

## Command

```bash
/arckit.secure Secure by Design assessment for <system>
```

Output: `projects/<id>/ARC-<id>-SECD-vX.Y.md`

> **Auto-versioning**: re-running increments the version (minor for refreshed assessment; major for materially changed scope).

---

## What The Assessment Covers

The assessment is structured around AU-aligned control areas:

- Governance, risk, and assurance (roles, risk acceptance, assurance gates, supplier assurance)
- Identity, access, and privilege management (MFA, PAM, least privilege, account lifecycle)
- Data protection and privacy (classification/handling, encryption and keys, retention/disposal, APPs, NDB readiness)
- Platform, network, and endpoint security (hardening, patching, segmentation, environment separation)
- Secure engineering and supply chain (secure SDLC, CI/CD checks, dependency risk, provenance/SBOM where appropriate)
- Logging, monitoring, and detection (coverage, retention, alerting, vulnerability management cadence)
- Incident response and resilience (playbooks, backups, recovery objectives, exercises)
- Cloud security and shared responsibility (if applicable), including IRAP readiness where required

---

## Essential Eight Mitigation Strategies

The output includes a maturity table for all eight strategies:

- Application control
- Patch applications
- Configure Microsoft Office macro settings
- User application hardening
- Restrict administrative privileges
- Patch operating systems
- Multi-factor authentication (MFA)
- Regular backups

---

## Privacy And NDB Readiness

If personal information is processed, the assessment includes:

- a summary of key APP areas relevant to the system and the evidence used
- whether a PIA exists (or a recommendation to perform one where risk is high)
- NDB readiness (detection and triage, “eligible data breach” decision process, notification approach and supplier notification expectations)

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

