# Module 03 — Automate the Boring Parts

**~2 hours · 5 lessons**

---

## What this module teaches

Hooks — code that runs automatically when Claude does something, so you don't have to.

Session opens → context re-injected. Session closes → work auto-committed. You type a keyword → Claude loads the right files without being told.

This is the module where Claude starts running without you.

---

## Before we start: git

You need to understand undo before you let hooks touch your files automatically. Lesson 3.1 covers git as a safety net — not as a developer tool, but as a time machine.

---

## Lessons

| # | Lesson | What you do |
|---|--------|-------------|
| 3.1 | [Git: The Undo Button](./3.1-git-undo/CLAUDE.md) | Commits = strata you read back |
| 3.2 | [Fault Lines](./3.2-fault-lines/CLAUDE.md) | What hooks are and what triggers them |
| 3.3 | [You Left, It Worked](./3.3-machine-wakes-up/CLAUDE.md) | Session-start hook + cron (explicitly distinct) |
| 3.4 | [Customize Routing](./3.4-routing/CLAUDE.md) | Intent routing for your business context |
| 3.5 | [Never Lose Work](./3.5-auto-commit/CLAUDE.md) | Session-end auto-commit |

---

**Repo used:** [`claude-code-hooks-kit`](https://github.com/singhjitesh889-blip/claude-code-hooks-kit) (7 hooks)

**Start:** `/start-3-1`
