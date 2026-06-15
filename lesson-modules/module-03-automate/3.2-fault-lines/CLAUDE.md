# Lesson 3.2: Fault Lines

In geology, a fault line is where the earth moves itself — not because you pushed it, but because the pressure built up to the point where the system had to shift.

Hooks are your fault lines.

They fire automatically — at specific moments — without you doing anything.

---

## What Hooks Are

Hooks are shell scripts that run when certain events happen in Claude Code:

- **session-start** — fires when you open Claude Code
- **user-prompt-submit** — fires before every prompt you send
- **post-tool-use** — fires after Claude uses a tool (read, write, bash, etc.)
- **session-end** — fires when you close Claude Code

They're in `~/.claude/hooks/` — they apply to every Claude Code project on your machine.

The `claude-code-hooks-kit` repo by Jitesh Kumar Singh (singhjitesh889-blip) has 7 production-ready hooks. That's what we'll use.

STOP: Ask me to show you what a hook file looks like.

USER: Asks

ACTION: Show the structure of a simple hook. For example, session-start.sh would look like:
```bash
#!/bin/bash
# session-start.sh — runs when you open Claude Code
# Injects fresh context so Claude knows what it's working with

echo "Loading Nimbu Fresh context..."
cat "$HOME/Desktop/PersonalProjects/strata/company-context/NIMBU-STATE.md"
```
Explain: "This script runs every time you type `claude`. Before your first message, it re-injects the STATE. Claude already knows your business before you say a word."

---

STOP: [BANTER] The ops team was writing their log every day into the void because nobody was reading it. The session-start hook is what makes sure your STATE is never ignored.

USER: continues

---

**Next up:** 3.3 — the machine wakes up. Session-start hook vs. cron — two different tools, one important distinction.

STOP: Ready? Type /start-3-3

USER: /start-3-3

---

## Success Criteria
- [ ] Student understands what hooks are (shell scripts firing on events)
- [ ] Student knows the 4 main hook types
- [ ] Student understands where hooks live (~/.claude/hooks/)
- [ ] Student has seen what a hook file looks like
- [ ] Geology/fault-line metaphor landed
