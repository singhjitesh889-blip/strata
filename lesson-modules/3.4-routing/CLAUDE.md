# Lesson 3.4: Customize Routing

The user-prompt-submit hook fires before every message you send.

This means you can intercept your own prompts and inject relevant context before Claude even reads them.

---

## The Routing Idea

When you type "ops update" — Claude should automatically load the ops files.
When you type "campaign review" — Claude should load the campaign files.
When you type "founder update" — it should run /founder-update directly.

Without routing, you have to remember to @ every file every time. With routing, it's automatic.

STOP: Ask me to create a user-prompt-submit hook that detects keywords and injects relevant context.

USER: Asks for routing hook

ACTION: Create ~/.claude/hooks/user-prompt-submit.sh:
```bash
#!/bin/bash
# user-prompt-submit — intent-based context routing for Nimbu Fresh
PROMPT="$1"

if echo "$PROMPT" | grep -qi "ops\|operations\|delivery\|courier\|stock\|inventory"; then
  echo "Loading ops context..."
  cat "$HOME/Desktop/PersonalProjects/strata/analysis/ops-intelligence-june.md" 2>/dev/null
fi

if echo "$PROMPT" | grep -qi "campaign\|roas\|ads\|spend\|mango\|reels"; then
  echo "Loading campaign context..."
  cat "$HOME/Desktop/PersonalProjects/strata/analysis/campaign-ranking-report.md" 2>/dev/null
fi

if echo "$PROMPT" | grep -qi "founder\|vikram\|update\|slide"; then
  echo "Routing to founder-update command..."
fi
```
chmod +x the file. Explain each section.

---

STOP: Test it. Type: "ops mein kya chal raha hai?" — what context gets injected?

USER: Ops files / something ops-related

"The routing detected 'ops' in your prompt and automatically loaded the ops intelligence. You didn't @ anything."

---

**Next up:** 3.5 — never lose work. The session-end auto-commit hook.

STOP: Ready? Type /start-3-5

USER: /start-3-5

---

## Success Criteria
- [ ] user-prompt-submit.sh created with keyword routing
- [ ] Student tested routing with an ops prompt
- [ ] Student understands how hooks intercept and augment prompts
