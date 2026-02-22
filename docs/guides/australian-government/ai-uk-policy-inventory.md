# AI-002 — UK Policy/Concept Inventory in AI Scope

Branch: `feat/au-ai-first-principles`  
Date: 2026-02-15  
Scope: files listed in `ai-file-inventory.md` (AI-only surfaces + relevant wiring)

## Method

- Read AI-scope files end-to-end (including long JSP-936 prompt/command surfaces).
- Collated UK policy/concept references with exact file+line anchors.
- Grouped duplicates where plugin mirrors are byte-identical or prompt/command near-mirrors.

> Disposition meanings:  
> **replace** = AU-first equivalent required in default paths.  
> **retain-as-legacy** = keep only in explicit UK legacy paths/surfaces.  
> **delete** = remove from AU AI scope (no AU replacement needed in these files).

## Inventory

| # | UK policy/concept | Why it matters in current ArcKit logic | Exact file references (line anchors) | Initial disposition |
|---|---|---|---|---|
| 1 | UK Government AI Playbook (10 principles + 6 ethical themes) | Core assessment framework for `/arckit.ai-playbook`; also referenced by MLOps, ATRS, and JSP-936 flows. | `.arckit/templates/uk-gov-ai-playbook-template.md:1,10,46,734`<br>`.codex/prompts/arckit.ai-playbook.md:2,5,196,255-262,467-488`<br>`docs/guides/ai-playbook.md:3,34-52,85-91`<br>`docs/guides/uk-government/ai-playbook.md:1-3`<br>`arckit-plugin/commands/ai-playbook.md:2,5,196,255-262,467-488` | replace |
| 2 | Algorithmic Transparency Recording Standard (ATRS) | Public transparency artifact is mandatory in AI governance flow; linked from AI Playbook and MLOps. | `.arckit/templates/uk-gov-atrs-template.md:1,38-52,657,932,944`<br>`.arckit/templates/uk-gov-ai-playbook-template.md:577,583-584,760,811`<br>`.codex/prompts/arckit.atrs.md:2,15-18,214,378-399`<br>`docs/guides/atrs.md:3,28-46,84`<br>`docs/guides/uk-government/algorithmic-transparency.md:1-3,36,42` | replace |
| 3 | MOD JSP 936 (Dependable Artificial Intelligence in Defence) | Primary defence AI assurance framework; drives dedicated command/template, lifecycle evidence, and approvals. | `.arckit/templates/jsp-936-template.md:1,10,654-666,1103-1107,1233`<br>`.codex/prompts/arckit.jsp-936.md:9-18,617,1695-1727,3393`<br>`docs/guides/jsp-936.md:1-3,32-35`<br>`.arckit/templates/mlops-template.md:642-649`<br>`arckit-plugin/commands/jsp-936.md:10-18,618,1696-1727,3394` | retain-as-legacy |
| 4 | RAISO (Responsible AI Senior Officer) role | Hard-coded governance role across JSP-936 assurance, approvals, and monitoring cadence. | `.arckit/templates/jsp-936-template.md:254,700,735,1077,1132`<br>`.codex/prompts/arckit.jsp-936.md:357,675,1588,2008-2015,3311`<br>`docs/guides/jsp-936.md:14,35,55`<br>`docs/guides/uk-government/ai-playbook.md:24` | retain-as-legacy |
| 5 | UK MOD approval authorities (2PUS, JROC/IAC, TLB) | Determines risk classification pathway and who can approve deployment/re-approval. | `.arckit/templates/jsp-936-template.md:178-184,205,726-730`<br>`.codex/prompts/arckit.jsp-936.md:17,224-228,2040-2044,3420-3426`<br>`docs/guides/jsp-936.md:32`<br>`.arckit/templates/mlops-template.md:649` | retain-as-legacy |
| 6 | JSP 440 MOD security policy linkage | Defence security handling baseline repeatedly tied to JSP-936 assurance package. | `.arckit/templates/jsp-936-template.md:971`<br>`.codex/prompts/arckit.jsp-936.md:1745,2607,2645,2711,3382`<br>`scripts/bash/create-project.sh:172`<br>`src/arckit_cli/__init__.py:525` | retain-as-legacy |
| 7 | UK Secure by Design (civil + MOD variants) | AI files and wiring assume Secure-by-Design assessments as companion evidence. | `.arckit/templates/jsp-936-template.md:832,1144`<br>`.codex/prompts/arckit.jsp-936.md:67,2396,2448,2608,3225`<br>`docs/guides/uk-government/ai-playbook.md:22-23`<br>`scripts/bash/create-project.sh:249,309`<br>`src/arckit_cli/__init__.py:524-525` | replace |
| 8 | Technology Code of Practice (TCoP) | Cross-linked governance dependency in AI Playbook/ATRS logic and command wiring. | `.arckit/templates/uk-gov-atrs-template.md:793`<br>`.codex/prompts/arckit.ai-playbook.md:301-304,478`<br>`.codex/prompts/arckit.atrs.md:192,236,390`<br>`scripts/bash/create-project.sh:250,308`<br>`src/arckit_cli/__init__.py:519` | replace |
| 9 | GDS Service Standard | Referenced as required adjacent assessment context for AI transparency/compliance. | `.arckit/templates/uk-gov-atrs-template.md:795`<br>`.codex/prompts/arckit.atrs.md:192,392`<br>`.codex/prompts/arckit.ai-playbook.md:480`<br>`src/arckit_cli/__init__.py:518` | replace |
| 10 | Data Ethics Framework | Embedded as explicit compliance criterion in AI Playbook/ATRS flows. | `.arckit/templates/uk-gov-ai-playbook-template.md:132`<br>`.arckit/templates/uk-gov-atrs-template.md:796`<br>`.codex/prompts/arckit.ai-playbook.md:119,479,488`<br>`.codex/prompts/arckit.atrs.md:192,391` | replace |
| 11 | UK GDPR | Baseline legal control in AI Playbook, ATRS, JSP-936 and secure command descriptions. | `.arckit/templates/uk-gov-ai-playbook-template.md:129,141`<br>`.arckit/templates/uk-gov-atrs-template.md:768`<br>`.arckit/templates/jsp-936-template.md:972`<br>`.codex/prompts/arckit.ai-playbook.md:117`<br>`src/arckit_cli/__init__.py:524` | replace |
| 12 | Data Protection Act 2018 (DPA 2018) | Defence and transparency artifacts explicitly call this out for lawful processing/security obligations. | `.arckit/templates/uk-gov-atrs-template.md:769`<br>`.codex/prompts/arckit.atrs.md:367`<br>`.codex/prompts/arckit.jsp-936.md:662,2609,2646,2712,3360`<br>`arckit-plugin/commands/jsp-936.md:663,2610,2647,2713,3361` | replace |
| 13 | Equality Act 2010 | Explicit fairness/equality legal check in AI Playbook + ATRS compliance sections. | `.arckit/templates/uk-gov-ai-playbook-template.md:130,142`<br>`.arckit/templates/uk-gov-atrs-template.md:770`<br>`.codex/prompts/arckit.ai-playbook.md:118` | replace |
| 14 | Public Sector Equality Duty | Mandatory equality-duty concept baked into AI legal/ethical checklisting. | `.arckit/templates/uk-gov-ai-playbook-template.md:131`<br>`.arckit/templates/uk-gov-atrs-template.md:773` | replace |
| 15 | Human Rights Act 1998 / ECHR framing | Human-rights checks are explicitly required in AI and ATRS guidance text. | `.arckit/templates/uk-gov-atrs-template.md:449,771`<br>`.codex/prompts/arckit.ai-playbook.md:349`<br>`.codex/prompts/arckit.atrs.md:147` | replace |
| 16 | Freedom of Information Act 2000 | Included in ATRS legal compliance matrix for publication/transparency context. | `.arckit/templates/uk-gov-atrs-template.md:772` (mirror: `arckit-plugin/templates/uk-gov-atrs-template.md:772`) | replace |
| 17 | Mandatory assessment stack (PIA, EqIA, Human Rights assessment) | Treated as blocking criteria in AI Playbook/ATRS command logic for high-risk systems. | `.arckit/templates/uk-gov-ai-playbook-template.md:126-128,138-139,812-814`<br>`.arckit/templates/uk-gov-atrs-template.md:401-447,920-922`<br>`.codex/prompts/arckit.ai-playbook.md:116,276-278,312,338-347`<br>`.codex/prompts/arckit.atrs.md:145-147,210-211,242-243` | replace |
| 18 | ICO AI Guidance / ICO consultation and registration | UK regulator-specific compliance and escalation path appears in prompts/templates. | `.arckit/templates/uk-gov-atrs-template.md:409,781`<br>`.codex/prompts/arckit.ai-playbook.md:482,489`<br>`.codex/prompts/arckit.atrs.md:191` | replace |
| 19 | NCSC guidance / CAF references | Security controls in AI governance are mapped to UK cyber guidance structures. | `.arckit/templates/uk-gov-ai-playbook-template.md:168`<br>`.arckit/templates/jsp-936-template.md:973`<br>`.codex/prompts/arckit.ai-playbook.md:123,481`<br>`src/arckit_cli/__init__.py:524` | replace |
| 20 | Cyber Essentials / Cyber Essentials Plus | UK certification requirement appears in ATRS/JSP-936 evidence checklists and CLI help text. | `.arckit/templates/uk-gov-atrs-template.md:391`<br>`.arckit/templates/jsp-936-template.md:964`<br>`.codex/prompts/arckit.jsp-936.md:2610,3243`<br>`src/arckit_cli/__init__.py:524` | replace |
| 21 | ISO assurance standards (ISO 27001 / ISO 9001) in UK governance framing | Used as referenced assurance controls in ATRS/JSP-936 compliance rows. | `.arckit/templates/uk-gov-atrs-template.md:392,798-799`<br>`.arckit/templates/jsp-936-template.md:964`<br>`.codex/prompts/arckit.jsp-936.md:2626,2692` | replace |
| 22 | Government Design Principles / CDDO guidance | UK central digital policy institutions are embedded in transparency/governance guidance. | `.arckit/templates/uk-gov-atrs-template.md:794`<br>`.codex/prompts/arckit.ai-playbook.md:163`<br>`docs/guides/atrs.md:83` | replace |
| 23 | AI Standards Hub and cross-government collaboration concept | Collaboration principle is framed around specific UK public-sector institutions. | `.arckit/templates/uk-gov-ai-playbook-template.md:380`<br>`.codex/prompts/arckit.ai-playbook.md:163`<br>`docs/guides/uk-government/ai-playbook.md:27` | replace |
| 24 | ALB/central department scope rule for mandatory AI transparency | ATRS applicability is explicitly tied to UK public-body structure. | `.arckit/templates/uk-gov-atrs-template.md:39-40`<br>`.codex/prompts/arckit.atrs.md:16`<br>`.codex/prompts/arckit.ai-playbook.md:333-334` | replace |
| 25 | DSIT ATRS contact + GOV.UK ATRS publication workflow | UK-specific publication endpoint/contact hardcoded into ATRS guidance and completion steps. | `.arckit/templates/uk-gov-atrs-template.md:52,932,944`<br>`.codex/prompts/arckit.atrs.md:337,379,385,398-399`<br>`arckit-plugin/commands/atrs.md:337,379,385,398-399` | delete |
| 26 | G-Cloud / DOS procurement frameworks | UK procurement frameworks leak into AI transparency + wiring surfaces. | `.arckit/templates/uk-gov-atrs-template.md:153,803`<br>`.codex/prompts/arckit.atrs.md:111`<br>`scripts/bash/migrate-filenames.sh:52-53`<br>`docs/manifest.json:251,256,260-261`<br>`src/arckit_cli/__init__.py:492-494` | delete |
| 27 | IR35 compliance | UK contractor tax-rule reference appears in ATRS procurement compliance section. | `.arckit/templates/uk-gov-atrs-template.md:807`<br>`.codex/prompts/arckit.atrs.md:193` | delete |
| 28 | UK “Public Task” lawful-basis framing | UK-specific lawful basis taxonomy appears in legal sections and worked examples. | `.arckit/templates/uk-gov-ai-playbook-template.md:145`<br>`.arckit/templates/uk-gov-atrs-template.md:788`<br>`.codex/prompts/arckit.atrs.md:367` | replace |
| 29 | MOD adjunct security frameworks (CAAT, IAMM) | UK defence security references embedded in AI project scaffolding/help text. | `scripts/bash/create-project.sh:172`<br>`src/arckit_cli/__init__.py:525` | retain-as-legacy |

---

## Coverage notes

- Plugin mirrors for templates/guides/scripts were included where content is duplicated.
- Prompt ↔ plugin-command near-mirror pairs were validated; policy-bearing content is effectively duplicated across both surfaces.
- No UK references in this inventory were intentionally omitted from AI-scoped files.
