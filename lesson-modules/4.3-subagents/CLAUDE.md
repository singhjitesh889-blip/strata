# Lesson 4.3: Subagents — Your Specialist Advisory Board

In 1.6, we used agents for parallel processing — temporary workers for simultaneous tasks.

Subagents are different. They're permanent.

A subagent has a defined personality, perspective, and area of expertise. They live in `.claude/agents/`. They're always available.

---

## Your Advisory Board

Three subagents are already installed in this course:

STOP: Ask me to introduce you to the three advisors already installed in .claude/agents/.

USER: Asks for introductions

ACTION: Read all three agent files. Introduce each one in character:

**Skeptical CFO:** "Will this move EBITDA? Not impressions — EBITDA. Show me CAC, show me unit economics, show me what stops this from scaling."

**Growth Lead:** "Where's the D2C hook? What's the repeat rate? Are we building a customer base or a one-time purchase list?"

**Ops Manager:** "Main ground pe hoon. Packaging wala issue 8 baar aaya June mein. Yeh kab fix hoga?"

---

## The Review

STOP: Ask all three subagents to review the founder-update-jun-2026.md from their perspectives. What does each one flag?

USER: Asks for multi-agent review

ACTION: Run all three agents on the founder update. Each reviews from their own lens:
- CFO: "The ROAS is good. What's the CAC? What's the second-order purchase rate on Mango buyers?"
- Growth Lead: "14 customers asked for subscriptions. Why isn't this in the recommendation section?"
- Ops Manager: "Packaging resolved is marked as 'monitor in July.' WHO is monitoring? Specific person?"

Save to reviews/founder-update-advisory-review.md

---

## Create Your Own

STOP: The /agents command lets you create new subagents. You could build: a "confused customer" to stress-test your communication clarity, a "CA advisor" who knows GST rules, a "Vikram voice" who reviews updates the way Vikram would.

Try /agents to see the flow — or tell me what kind of advisor you want and I'll build the file.

USER: Tries /agents / requests a specific advisor / says continue

ACTION: If they want a specific advisor, build the .md file for it in .claude/agents/. Show the format.

---

**Next up:** 4.4 — the orchestrator pattern. One goal, a fleet of specialists.

STOP: Ready? Type /start-4-4

USER: /start-4-4

---

## Success Criteria
- [ ] Student met all three subagents in character
- [ ] All three reviewed the founder update from their perspectives
- [ ] reviews/founder-update-advisory-review.md created
- [ ] Student understands agents (temporary) vs subagents (permanent)
- [ ] Student knows /agents command to create their own
