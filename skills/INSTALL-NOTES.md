# INSTALL-NOTES — Awesome Muse Skills (manager's picks)

- **Source:** https://github.com/aicodedecode/awesome-muse-skills
- **License:** MIT (Awesome Muse Skills contributors)
- **Original repo size:** 123M (full catalog, kept locally as the hiring bank — NOT included in this repo)
- **Catalog contents:** 2,648 skills (899 original + 1,749 curated imports) in Agent Skills format (SKILL.md + YAML frontmatter).

## What is installed: 26 skills (not the whole catalog)

The whole catalog was NOT installed — most of it is irrelevant to an
office's work (hundreds of programming-language, bioinformatics, and
other domain skills). The installed set is the office manager's
selection, each copied verbatim into `skills/<name>/` together with
`skill.yaml`, `INSTALL-NOTES.md`, and `ATTRIBUTION.md`:

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

- The catalog's domain-specific skills (programming languages,
  science, and other specialties) — hire them later, when a task
  actually needs one, through the `skill-curator` process.
- Any skill that duplicates a capability the office already has
  from another source.

## The catalog as a hiring bank

The full catalog is kept locally as the manager's hiring bank (not in
this repo). When a task needs an expertise the office does not have
yet, the manager searches the catalog (`skills/` for originals,
`skills-imported/` for curated imports), reads its SKILL.md, then
installs it following the `skill-curator` process (read-only shallow
clone, frontmatter validation, security scan, never run repo code or
installers, dedupe by content).

## Local adaptations (apply to all 26 skills)

- These skills were written for local/CLI agents. In Muse, "agent"
  means a Muse sub-agent, and "fleet" means the agents of the Virtual
  Office (GRANTS, COMPLIANCE, MENTORING, TEACHING, RESEARCH, CONTENT,
  REVIEW).
- Commands referring to local CLI tools that do not exist in this VM
  are not used; they are replaced with the equivalent Muse tool.
- The owner's rules always win: no sending messages/emails on the
  owner's behalf without approval; no paid costs without approval;
  sensitive case content only in its dedicated chat.

## Desk mapping (rough)

- GRANTS (Grants & funding): email-triage, scheduling-assistant,
  forms-pro, survey-designer.
- COMPLIANCE (Rules & compliance): meeting-notes-ai, document-parser.
- MENTORING (Mentoring & supervision): citation-manager, docx-pro,
  pdf-pro.
- TEACHING (Teaching & classes): presentation-designer, weekly-review.
- RESEARCH (Research & reading): docs-search, memory-search,
  citation-manager.
- CONTENT (Content & media): content-strategist, social-media-manager,
  newsletter-pro, daily-briefing.
- REVIEW (Evaluation & data): task-manager, weekly-review,
  presentation-designer.
- Manager (Muse): agent-manager-skill, agent-management,
  agent-orchestration, agent-messaging, planning, skill-creator,
  skill-curator, calendar-guardian, task-manager.
