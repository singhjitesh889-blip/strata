# STRATA

**The first Claude Code course built for Indian knowledge workers.**

Brand managers. MBAs. Growth leads. FMCG operators. People who work in Excel and ChatGPT and want the next level — without learning to code.

---

## What You'll Build

You're the new Growth Lead at **Nimbu Fresh** — a fictional D2C juice startup. The previous person quit Friday. No handoff. You inherited:

- 11 ad CSVs all named `FINAL_v2_USE_THIS_[n].csv`
- 200 lines of Hinglish ops chaos in a text file
- A GST sheet nobody opened since February
- A founder who texts "ROAS?? 🤔" on Sunday night

By the end of Module 1, you'll have a clean, source-verified founder update built from all of that. In under 20 minutes. Without opening Excel once.

By the end of Module 6, you'll have a system that ranks your campaigns, knows your business context, and sends you a Telegram digest before your founder asks.

---

## Quick Start

```bash
# First time? Read SETUP.md — it gets you from zero to terminal in 15 minutes
git clone https://github.com/singhjitesh889-blip/strata.git
cd strata
claude
/start-0
```

That's it. The course runs inside Claude Code. No browser. No video. No slides.

---

## Course Structure

| Module | Title | What You Learn | Duration |
|--------|-------|----------------|----------|
| 0 | Grade Select | Who you are, how to pace | 5 min |
| 1 — Kaam Shuru Karo | [Inherit the Chaos](./lesson-modules/module-01-inherit-the-chaos/) | Daily wins — 11 CSVs → clean founder update | ~3.5 hrs |
| 2 — Dimaag Banao | [Give It a Memory](./lesson-modules/module-02-give-it-memory/) | RAW → WIKI → STATE knowledge architecture | ~2 hrs |
| 3 — Khud Chale | [Automate the Boring Parts](./lesson-modules/module-03-automate/) | Hooks — the system that runs itself | ~2 hrs |
| 4 — Asli Taakat | [Wire It to Live Data](./lesson-modules/module-04-live-data/) | MCP servers — Claude with live data | ~1 hr |
| 5 — Asli Taakat | [Delegate the Work](./lesson-modules/module-05-delegate/) | Subagents, orchestrator, agentic loops | ~2 hrs |
| 6 — Asli Taakat | [Verify Everything](./lesson-modules/module-06-verify/) | Boris's 5-step loop — eval gate + ground-truth | ~1.5 hrs |

27 lessons. 6 modules. All taught by Claude Code inside your terminal.

---

## Repos This Course Uses

These are Jitesh's open-source repos. The course walks you through each one:

| Repo | What It Does | Course Module |
|------|-------------|---------------|
| [claude-code-knowledge-architecture](https://github.com/singhjitesh889-blip/claude-code-knowledge-architecture) | RAW→WIKI→STATE knowledge system | Module 2 |
| [claude-code-hooks-kit](https://github.com/singhjitesh889-blip/claude-code-hooks-kit) | 7 production hooks for Claude Code | Module 3 |
| [mcp-commerce-starter](https://github.com/singhjitesh889-blip/mcp-commerce-starter) | MCP server: 22 tools, 1,134 lines | Modules 4–6 |
| [mcp-seo-starter](https://github.com/singhjitesh889-blip/mcp-seo-starter) | MCP server: 7 SEO tools, 495 lines | Modules 4–6 |

You don't need to clone any of these now. The course tells you when and how.

---

## Project Structure

```
strata/
├── SETUP.md                        # Start here if you've never used a terminal
├── GETTING-STARTED.md              # Quick start for experienced users
├── README.md                       # This file
├── progress.md                     # Written by L0, updated as you complete lessons
├── course-structure.json           # Full course map (lesson IDs, paths, commands)
│
├── .claude/
│   ├── SCRIPT_INSTRUCTIONS.md      # How Claude teaches each lesson
│   ├── commands/                   # /start-0 through /start-6-3 + /founder-update
│   └── agents/
│       ├── skeptical-cfo.md        # "Will this move EBITDA?"
│       ├── growth-lead.md          # "What's the repeat rate?"
│       └── ops-manager.md          # "Ground level — here's what's actually happening"
│
├── company-context/
│   ├── SCENARIO.md                 # Who Nimbu Fresh is, why you're there
│   ├── BRAND-VOICE.md              # How the brand sounds
│   └── PRODUCT-CATALOG.md          # SKUs, pricing, stock alerts
│
├── inherited-chaos/                # The mess waiting for you on day one
│   ├── ad-csvs/                    # 11 CSVs named FINAL_v2_USE_THIS_[n].csv
│   ├── ops-log/                    # ops-log-june.txt — 200 lines of Hinglish chaos
│   ├── gst-sheet/                  # gst-liability-q1.csv — unopened since February
│   ├── old-campaigns/              # 9 past campaign briefs
│   └── competitor-research/        # 5 Indian D2C juice brand snapshots
│
├── lesson-modules/
│   ├── module-01-inherit-the-chaos/   # 9 lessons (1.1–1.9) + grade select
│   ├── module-02-give-it-memory/      # 5 lessons (2.1–2.5)
│   ├── module-03-automate/            # 5 lessons (3.1–3.5)
│   ├── module-04-live-data/           # 2 lessons (4.1–4.2)
│   ├── module-05-delegate/            # 3 lessons (5.1–5.3)
│   └── module-06-verify/              # 3 lessons (6.1–6.3)
│
├── templates/                      # Reference outputs — what good looks like
│   ├── founder-update-template.md
│   ├── ops-intelligence-template.md
│   └── campaign-ranking-template.md
│
├── analysis/                       # You fill this as you work through the course
├── reviews/                        # Eval gate outputs land here
└── organized/                      # Cleaned, compiled outputs (fills with cohort)
```

---

## Grade System

At the start, you pick your grade:

- **G1 — Seedhi Baat:** Never used a terminal. Excel + ChatGPT only. Every step is explained.
- **G3 — Boss Level:** Already uses Claude or VS Code. Watch for `[G3: skip to ___]` markers to fast-forward past basics.

---

## Prerequisites

- A laptop (Mac, Windows with WSL2, or Linux)
- A Claude Max subscription or Anthropic API key
- About 15 minutes to complete setup

See `SETUP.md` for exact steps — from "what is a terminal" to `/start-0`.

---

## The Pitch

> *"By the end, you'll have a system that ranks your campaigns, knows your business context, and sends you a Telegram digest before your founder asks. You're not learning to code. You're learning to never open 11 spreadsheets again."*

---

## Creator

**Jitesh Kumar Singh** — BSc Geology (BHU) + MBA Marketing (IIM Udaipur) + Product Brand Manager

Portfolio: [singhjitesh889-blip.vercel.app](https://singhjitesh889-blip.vercel.app)

---

## License

MIT — use, adapt, share freely. Credit appreciated, not required.
