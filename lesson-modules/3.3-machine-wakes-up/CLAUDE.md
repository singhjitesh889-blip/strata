# Lesson 3.3: You Left, It Worked

Two different tools. One important distinction. Get this wrong and you'll build something that doesn't do what you think it does.

---

## Session-Start Hook ≠ Cron

**Session-start hook:**
- Fires when YOU open Claude Code
- Lives in `~/.claude/hooks/session-start.sh`
- Requires you to be there (you open the terminal, you type `claude`)
- Good for: injecting context, loading STATE, reminding you of current priorities

**Cron job:**
- Fires on a clock schedule (7am every day, regardless of what you're doing)
- Lives in `crontab -e`
- Requires your machine to stay on and connected
- Good for: morning ops reports, scheduled data pulls, daily digests

STOP: [QUIZ] If I install a session-start hook and close my laptop — does it run at 7am tomorrow?

USER: No / only when I open Claude / I don't know

[If No: "Correct. It only fires when YOU open Claude Code. Not on a schedule. Not automatically without you."]
[If unsure: "No. The session-start hook fires when you open Claude Code. Your laptop being closed = no hook runs. For autonomous scheduled runs, you need cron."]

---

## Install the Session-Start Hook

STOP: Ask me to install the session-start hook from claude-code-hooks-kit so that the NIMBU-STATE.md is injected every time you open Claude Code in this folder.

USER: Asks for installation

ACTION: Create ~/.claude/hooks/session-start.sh:
```bash
#!/bin/bash
# session-start — injects Nimbu Fresh STATE at session start
STATE_FILE="$HOME/Desktop/PersonalProjects/strata/company-context/NIMBU-STATE.md"
if [ -f "$STATE_FILE" ]; then
  echo "=== NIMBU FRESH STATE ==="
  cat "$STATE_FILE"
  echo "========================="
fi
```
Run: chmod +x ~/.claude/hooks/session-start.sh
Explain: "Now every time you open Claude Code from the strata folder, this runs first."

---

## Optional: Cron for Autonomous Reports

If you want something to run WITHOUT you present — like a morning ops summary at 9am — that's cron.

```bash
crontab -e
```
Add a line:
```
30 3 * * * cd /Users/you/Desktop/PersonalProjects/strata && python3 ops-report.py >> ops-cron.log 2>&1
```
(30 3 = 9am IST = 3:30am UTC)

The machine needs to stay on. This is how meta-pulse works — daily Python script, cron-scheduled, Telegram digest when complete.

STOP: [CHECKPOINT] To summarize: session-start hook fires when you ___. Cron fires when ___.

USER: open Claude / on a schedule

"Good. Two tools, different triggers, different use cases. Now you know which to reach for."

---

**Next up:** 3.4 — customizing routing so the right context loads for the right request.

STOP: Ready? Type /start-3-4

USER: /start-3-4

---

## Success Criteria
- [ ] Session-start hook vs cron distinction explicitly taught and confirmed
- [ ] session-start.sh installed and working
- [ ] Student understands cron as the autonomous scheduling mechanism
- [ ] "You left, it worked" aha: context loads automatically next time they open Claude
