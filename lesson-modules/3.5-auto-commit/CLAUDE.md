# Lesson 3.5: Never Lose Work

Every session end, you should have a commit.

Not because you remember to make one — but because the system makes one for you.

This is safe because Lesson 3.1 taught you undo. You know how to go back. Now you can go forward automatically.

---

STOP: Ask me to install the session-end auto-commit hook.

USER: Asks for the hook

ACTION: Create ~/.claude/hooks/session-end.sh:
```bash
#!/bin/bash
# session-end — auto-commit everything at session close
STRATA_DIR="$HOME/Desktop/PersonalProjects/strata"
if [ -d "$STRATA_DIR/.git" ]; then
  cd "$STRATA_DIR"
  git add .
  TIMESTAMP=$(date '+%Y-%m-%d %H:%M')
  git commit -m "session $TIMESTAMP — auto-commit" 2>/dev/null || true
fi
```
chmod +x the file.

---

STOP: Close Claude Code and reopen it. Then run `git log` — what do you see?

USER: Sees a new commit / describes the log

"Your stratigraphic column just grew by one layer. Automatically. Every session leaves a trace."

---

## Module 3 Complete

You now have:
- Git as your undo button (3.1)
- Hooks installed and running (3.2)
- Session-start context injection (3.3)
- Intent-based prompt routing (3.4)
- Auto-commit at session end (3.5)

The system runs itself. You open Claude — context loads. You work — routing helps. You close — commit happens.

STOP: [BANTER] The previous Growth Lead's CLAUDE.md had zero rules. Their git log was empty. Their ops log had 200 lines nobody read. You now have: 7 hooks, a memory architecture, and a commit history. Different setup.

USER: continues

STOP: Ready for Module 4 — Asli Taakat? This is where it gets genuinely powerful. Type /start-4-1

USER: /start-4-1

---

## Success Criteria
- [ ] session-end.sh installed
- [ ] Student tested it (close + reopen + git log)
- [ ] Module 3 completion feeling strong
- [ ] Student understands the autonomous system they've built
- [ ] Ready and excited for Module 4
