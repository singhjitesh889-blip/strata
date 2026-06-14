# Lesson 2.2: Write Your STATE Layer

The STATE is the briefing doc Claude reads every session.

Not a summary of everything. Not a data dump. The essential read — what Claude needs to be useful immediately.

Rule: ≤800 tokens. If it needs more than 800 tokens, you're including things that belong in WIKI, not STATE.

STOP: Let's build the Nimbu Fresh STATE layer together. Tell me: what are the 5 most important things Claude would need to know to be useful from the first message of any session?

USER: Answers — Vikram/founder, ROAS situation, best campaigns, ops status, etc.

[React to their list. Help them refine it.]

---

STOP: Ask me to create company-context/NIMBU-STATE.md with everything Claude needs to know at session start: who Vikram is, what the business is, the current performance snapshot, key rules from CLAUDE.md so far, and any active ops flags.

USER: Asks for STATE creation

ACTION: Create company-context/NIMBU-STATE.md:

```markdown
# Nimbu Fresh — STATE
Last updated: [today's date]

## Business Context
Nimbu Fresh: D2C juice startup, Bangalore. Growth Lead role. Vikram Bhatnagar = founder (IIT/BCG), texts at 11pm, wants one number not a dashboard.

## Current Performance (June 2026)
- Best campaign: Mango Launch (8.4x avg ROAS, Reels format)
- Spike: Reels Ad v2 June 7 (9.2x — "squeeze fresh" hook in first 2 seconds)
- Weak: Jeera Lemon (3.8x), Competitor Comparison (paused — legal)
- Independence Day worked last year — plan by August 1

## Ops Flags (June)
- Packaging: Mango cap issue, 8 complaints, resolved June 22 (new caps). Monitor July.
- Subscription demand: 14 customers asked this month. No product yet.
- Lucknow hub: resolved June 21.

## Key Rules (from CLAUDE.md)
[Include any rules student has added so far]

## Analysis Files Available
- analysis/campaign-ranking-report.md
- analysis/ops-intelligence-june.md
- analysis/ops-campaign-correlation.md
```

---

STOP: Read the STATE file you just built. Could Claude start a useful session just from this? Be honest.

USER: Yes / mostly / it's missing X

[If missing something: "Add it. The STATE should pass this test: I can read it and be useful immediately, without you having to explain anything."]
[If good: "That's the test. If yes — you've built your STATE layer."]

---

STOP: [CHECKPOINT] 800 tokens. Why that limit?

USER: Answers — performance / cost / focus

"Focus. The STATE is what you MUST know. If everything feels equally important, nothing is. The limit forces prioritization."

---

**Next up:** 2.3 — the WIKI layer. One file that answers one whole category of questions.

STOP: Ready? Type /start-2-3

USER: /start-2-3

---

## Success Criteria
- [ ] company-context/NIMBU-STATE.md created (≤800 tokens)
- [ ] Student understands STATE = essential read, not comprehensive dump
- [ ] The "could Claude be useful immediately from just this?" test passed
- [ ] Student ready for WIKI lesson
