# Lesson 4.5: Agentic Loops — The Machine That Reruns

Same upfront honesty as the last lesson.

Agentic looping is not a built-in Claude Code feature. There is no "loop mode." It's a pattern you build: give Claude a goal, a verification step, and the instruction to retry if verification fails.

---

## Closed Loop vs Open Loop

**Closed loop** — bounded:
- Clear goal
- Clear verification step ("check your answer against the source file")
- Clear endpoint ("stop when all numbers are verified")
- Budget-safe, quality-high

**Open loop** — unbounded:
- Wide exploratory goal with no defined endpoint
- Expensive, produces slop without tight constraints
- We're not building this today

For Nimbu Fresh, closed loops are what pay off.

---

## Build the Loop

STOP: Ask me to run a closed loop on the campaign ranking — goal: verify every ROAS number in campaign-ranking-report.md against its source CSV file. Stop when all 11 are verified or flagged.

USER: Asks for the closed loop

ACTION: Run the verification loop:
1. Read campaign-ranking-report.md
2. For each campaign, find its source CSV
3. Recalculate ROAS from source data
4. Flag any discrepancy between reported and calculated
5. Fix any discrepancies found
6. Save verified version to analysis/campaign-ranking-verified.md
7. Report: X verified, Y fixed, Z flagged for manual review

Show the loop running. Show where it catches discrepancies.

---

STOP: [QUIZ] Closed loop or open loop: "Verify all campaign ROAS numbers against source CSVs and stop when done." Which is it?

USER: Closed loop

"Closed. Clear goal, clear verification, clear endpoint. That's the pattern."

---

STOP: [QUIZ] "Explore everything interesting about the Nimbu Fresh business and keep going until you find something worth acting on." Closed or open?

USER: Open

"Open. No defined endpoint. Could run forever. Good for brainstorming, not for reliable production output."

---

**Next up:** 4.6 — verification + eval gate. How to make Claude check its own work.

STOP: Ready? Type /start-4-6

USER: /start-4-6

---

## Success Criteria
- [ ] Student understands closed loop = pattern, not built-in feature
- [ ] Closed vs open loop distinction clear
- [ ] analysis/campaign-ranking-verified.md created
- [ ] Student ready for verification lesson
