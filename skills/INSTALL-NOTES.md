# INSTALL-NOTES — Awesome Muse Skills (manager's picks)

- **Installed:** 10 November 2026
- **Source:** https://github.com/aicodedecode/awesome-muse-skills
- **License:** MIT (Awesome Muse Skills contributors)
- **Original repo size:** 123M (full catalog, kept locally as the hiring bank — NOT included in this repo)
- **Catalog contents:** 2,648 skills (899 original + 1,749 curated imports) in Agent Skills format (SKILL.md + YAML frontmatter).

## What is installed: 26 skills (not the whole catalog)

The whole catalog was NOT installed — most of it is irrelevant to this office's work (hundreds of programming-language, bioinformatics, and other domain skills). The installed set is the office manager's selection, each copied verbatim into `skills/<name>/` together with `skill.yaml`, `INSTALL-NOTES.md`, and `ATTRIBUTION.md`:

**Manager core (9):** agent-manager-skill, agent-management,
agent-orchestration, agent-messaging, planning, memory-search,
docs-search, skill-creator, skill-curator.

**Office operations (7):** daily-briefing, task-manager,
meeting-notes-ai, email-triage, calendar-guardian,
scheduling-assistant, weekly-review.

**Documents (6):** document-parser, docx-pro, pdf-pro,
presentation-designer, forms-pro, survey-designer.

**Research / citations (1):** citation-manager.

**Content (3):** content-strategist, social-media-manager,
newsletter-pro.

## What was deliberately NOT installed

- `humanizer` from the catalog — the office already uses `humanizer-id`
  (more complete, UDINUS campus preset), installed 10 Nov 2026.
- Literature/paper research skills — the office already uses
  `academic-research-skills`.
- Video/motion skills — the office already uses `bang-motion`,
  `flat-ui-explainer`, `higgsfield-news-story`, `anything2explainer`.
- Deck skills — the office already uses `deck-design` (UHN template)
  and `data-report`.
- Hundreds of software-development, science, and other domain skills
  that this office does not use.

## The catalog as a hiring bank

The full catalog is kept locally as the manager's hiring bank (not in
this repo). When a task needs an expertise the office does not have yet,
the manager searches the catalog (`skills/` for originals,
`skills-imported/` for curated imports), reads its SKILL.md, then
installs it following the `skill-curator` process (read-only shallow
clone, frontmatter validation, security scan, never run repo code or
installers, dedupe by content).

## Local adaptations (apply to all 26 skills)

- These skills were written for local/CLI agents. In Muse, "agent"
  means a Muse sub-agent, and "fleet" means the agents of the Virtual
  Office (BIMA, SATYA, BIMBING, NGAJAR, RISET, KABAR, AUDIT).
- Commands referring to local CLI tools that do not exist in this VM
  are not used; they are replaced with the equivalent Muse tool.
- The boss's rules always win: no sending messages/emails on Bos's
  behalf without approval; no paid costs without approval; PPKPT only
  in the PPKPT chat; Dian's Bab 1 stays KEPT until supervisor feedback.

## Desk mapping (rough)

- BIMA (Beasiswa & Pemagangan): email-triage, scheduling-assistant,
  forms-pro, survey-designer.
- SATYA (Satgas PPKPT): meeting-notes-ai, document-parser.
- BIMBING (Skripsi): citation-manager, docx-pro, pdf-pro.
- NGAJAR (Pengajaran): presentation-designer, weekly-review.
- RISET: docs-search, memory-search, citation-manager.
- KABAR (Konten & Media): content-strategist, social-media-manager,
  newsletter-pro, daily-briefing.
- AUDIT (Evaluasi & Data): task-manager, weekly-review,
  presentation-designer.
- Manager (Kadal Budug): agent-manager-skill, agent-management,
  agent-orchestration, agent-messaging, planning, skill-creator,
  skill-curator, calendar-guardian, task-manager.
