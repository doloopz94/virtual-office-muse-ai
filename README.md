Baca dalam Bahasa Indonesia: [README.id.md](README.id.md)

# Virtual Office — Muse AI

A virtual office run by **Muse** (office manager "Kadal Budug") for **Bos Rifki** — seven desks, one task board, and a library of 26 manager skills. This repository contains a standalone, static rebuild of the office plus the skill library that powers it.

> **Honest note:** the live office runs inside Muse as a fullstack app, and it cannot be shared through a public link (its data is tied to the owner's account). This repo is a faithful, self-contained rebuild: the office app in `office/` runs offline from a single HTML file and stores its data in your browser's `localStorage`. It is a demo and a starting point — not the live office.

## Screenshots

![2D floor plan](docs/screenshots/denah-2d.png)
*2D floor plan — seven desks, one chibi character per unit, live WIB clock.*

![Task board](docs/screenshots/papan-tugas.png)
*Task board — Antre → Dikerjakan → Menunggu Bos → Selesai.*

![Recruit panel](docs/screenshots/panel-rekrut.png)
*Recruit panel — the installed skills and how hiring works.*

## The seven desks

| Desk | Unit | Scope |
|------|------|-------|
| 🎓 **BIMA** | Beasiswa & Pemagangan | KIP-K, scholarships, internships, financial reports (LPJ), SPI deck |
| 🛡️ **SATYA** | Satgas PPKPT | Campus violence-prevention task force — general administration only |
| 📚 **BIMBING** | Skripsi | Thesis mentoring (Dian & Izal) — mentor, not official supervisor |
| 🧑‍🏫 **NGAJAR** | Pengajaran | Programming Mobile (Kotlin/Android) & Web Design, online |
| 🔬 **RISET** | Riset | Research, literature search via free Consensus / OpenAlex connectors |
| 🎬 **KABAR** | Konten & Media | Daily news digests, Facebook content, reels proposals |
| 📊 **AUDIT** | Evaluasi & Data | Performance evaluation, data recaps, verified reports |

## How the task board works

Every assignment enters as a *Surat Tugas* (task letter) and moves through four columns:

**Antre → Dikerjakan → Menunggu Bos → Selesai**

- The office processor works on tasks in **Dikerjakan** (every 30 minutes in the live office).
- Finished work is delivered to the main chat and the task moves to **Menunggu Bos** — never to **Selesai** automatically.
- **Only Bos marks a task Selesai.**

### Manager autonomy (approved 10 Nov 2026)

- Tasks Bos writes himself run automatically, without pressing "Mulai kerjakan".
- Autonomy covers internal work only: drafts, documents, research, preparation.
- Anything that needs sending a message/email, posting, paying/subscribing, generating a video/reels package, or touching PPKPT case content goes to **Menunggu Bos** with a note explaining why Bos is needed.
- Deadline reminders for important/urgent tasks: at most once per task per day.
- The manager may hire **free** skills/agents on his own and reports each hire; paid hires stay candidates until Bos approves.

### Hard rule — SATYA

The office **never processes PPKPT case content** (names/initials of parties, minutes, recommendations, summons). Case work happens only in the dedicated PPKPT chat. The office only handles general administration: attendance lists, templates, schedules, letter numbering.

## ⭐ The highlight: 26 manager skills

The main focus of this repo is the **26 manager skills** chosen from the [Awesome Muse Skills](https://github.com/aicodedecode/awesome-muse-skills) catalog (MIT, 2,648 skills), installed on 10 November 2026. Each skill is copied **verbatim** into `skills/` with its `SKILL.md`, `skill.yaml`, `INSTALL-NOTES.md`, and `ATTRIBUTION.md`.

- **Manager core (9):** agent-manager-skill, agent-management, agent-orchestration, agent-messaging, planning, memory-search, docs-search, skill-creator, skill-curator
- **Office operations (7):** daily-briefing, task-manager, meeting-notes-ai, email-triage, calendar-guardian, scheduling-assistant, weekly-review
- **Documents (6):** document-parser, docx-pro, pdf-pro, presentation-designer, forms-pro, survey-designer
- **Research & citations (1):** citation-manager
- **Content (3):** content-strategist, social-media-manager, newsletter-pro

Details, groupings, desk mapping, and what was deliberately *not* installed: see [skills/INSTALL-NOTES.md](skills/INSTALL-NOTES.md).

## The standalone app

Open [`office/index.html`](office/index.html) directly in a browser — no build step, no server, no external dependencies, everything inline, works offline:

- **Denah** (`#denah`): 2D floor plan with seven desks and a chibi character per unit, live WIB clock, open-task counts.
- **Papan Tugas** (`#papan`): the four-column board with the 7 real seed tasks. Drag cards between columns, or use the move menu on each card (touch-friendly). Changes persist in `localStorage`.
- **Rekrut** (`#rekrut`): the hiring process and the 26 installed skills, grouped with their desk mapping.

Views are addressable by URL hash: `#denah` (default), `#papan`, `#rekrut`.

## Repository layout

```
.
├── README.md                  # This file (English)
├── README.id.md               # Bahasa Indonesia version
├── LICENSE                    # MIT
├── office/
│   └── index.html             # Standalone office app (single file, offline)
├── skills/
│   ├── INSTALL-NOTES.md       # The 26 skills: groups, desk mapping, what was skipped
│   └── <26 skill folders>/    # Verbatim copies: SKILL.md + skill.yaml + notes
└── docs/
    ├── brain.md               # The office brain: rules per unit, autonomy, hiring
    └── screenshots/           # 2D floor plan, task board, recruit panel
```

## Rules that govern this office

Full rules live in [docs/brain.md](docs/brain.md). The short version:

- Bahasa Indonesia. Address the boss as "Bos Rifki".
- Never send a message or email on Bos's behalf without his approval — draft first, Bos approves.
- Never fabricate data, numbers, citations, or names. If it is unverified, say so.
- Bos rests 12.00–13.00 WIB: no work scheduled in that hour.
- Instagram reels captions: max 120 **characters**.
- Deck rule: discuss the points in chat until one shared understanding, then build the deck.
- Video: rendered from code (Remotion / bang-motion), never AI video generation. Offer motion-style choices before generating.

## License

MIT — see [LICENSE](LICENSE). The skills in `skills/` are MIT-licensed from the Awesome Muse Skills contributors; each folder keeps its own `ATTRIBUTION.md`.
