# Lesson 2.5: Write Rules, Not Corrections

Here's how most people use Claude.

They get a wrong answer. They correct it. Claude fixes it. Next session — same wrong answer.

The correction didn't stick. You paid for it twice.

---

## The Habit

**Every mistake → CLAUDE.md. Not "fix it this time." Make it a rule.**

This is the difference between a tool that resets every session and one that gets sharper.

STOP: Open CLAUDE.md in this project (or ask me to show you what's in it). Read the rules you've added so far.

USER: Reads the rules / asks to see them

ACTION: Read the current CLAUDE.md. Show what's there. If it's sparse, that's fine — we're about to add to it.

---

## Review Your Session

STOP: Look back at what we've done in this course. Tell me: what's one thing I got wrong that you had to correct? Or one thing you wish I'd done differently by default?

USER: Names something — a format preference, a data issue, a tone thing, anything

ACTION: Take what they named and write it as a clean CLAUDE.md rule. Something like:
- "Always cite which file a number came from when giving campaign stats."
- "When showing campaign data, default to a table, not paragraphs."
- "Nimbu Fresh's revenue should always be shown ex-GST (divide by 1.05)."

Add it to CLAUDE.md. Show the addition.

---

## Formalizing the Architecture

STOP: Now — a more important rule. The STATE layer is at company-context/NIMBU-STATE.md. Ask me to add a rule to CLAUDE.md that tells me to read it at the start of every session.

USER: Asks for the rule

ACTION: Add to CLAUDE.md:
```
## Session Start
At the start of every session, read @company-context/NIMBU-STATE.md before responding to anything else. This is the briefing doc. Read it first.
```

Show the addition.

---

## The Test

STOP: Close this session. Start a new one. Type: "What's the packaging situation at Nimbu Fresh?"

USER: Does it / tells you what happened

[If Claude read the STATE and answered correctly: "It worked. You now have a Claude that knows your business before you say a word."]
[If it didn't work: Debug — check CLAUDE.md exists at project root, check the rule is correctly written, troubleshoot together.]

---

## Module 2 Complete

You built:
- A RAW → WIKI → STATE architecture for Nimbu Fresh
- A STATE file Claude reads every session
- WIKI files that answer questions with precision
- A compile loop that rewrites, not appends
- A CLAUDE.md that makes the system smarter every mistake

STOP: Module 2 done. Ready for Module 3 — Khud Chale. The system that runs itself. Type /start-3-1

USER: /start-3-1

---

## Success Criteria
- [ ] Student reviewed existing CLAUDE.md rules
- [ ] At least one new rule added based on actual session experience
- [ ] Session-start rule added (read NIMBU-STATE.md)
- [ ] Student tested it in a new session
- [ ] "Write rules, not corrections" principle fully internalized
- [ ] Student excited for Module 3
