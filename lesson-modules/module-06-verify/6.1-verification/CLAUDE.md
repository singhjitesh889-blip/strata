# Lesson 4.6: Verification + Eval Gate

Here's the highest-leverage habit in this entire course.

Give Claude a way to check its own output.

That single change produces 2-3x better quality on anything involving data.

---

## The 5-Step Verification Loop

Every piece of work — analysis, founder update, campaign recommendation — goes through this loop:

| Step | What it means |
|------|--------------|
| **1. Task** | Define the goal and success criteria BEFORE touching anything |
| **2. Execute** | Claude does the work |
| **3. Eval gate** | Claude checks its own output — are the numbers right? Is anything unsupported? |
| **4. Ground-truth** | YOU verify against an external source — not Claude rechecking itself |
| **5. Commit on PASS** | Only save/send/act if it passes. If FAIL → loop back to Step 1 with what you now know. |

The step most people skip: **Commit only on PASS**.

The step most people confuse: **Eval gate ≠ Ground-truth**. Eval gate is Claude reviewing its own output. Ground-truth is you (or a script) checking against the actual source. Different checks.

---

## Ground-Truthing

In geology: before relying on a surface reading, geologists drill to verify — ground-truthing. The surface can be misleading. The drill tells you what's actually there.

Eval gate = ask skeptical-cfo to review the analysis. Finds logical errors and unsupported claims.

Ground-truth = you open FINAL_v2_USE_THIS_1.csv yourself and check that the ROAS number Claude gave you matches what's actually in the file.

Both steps matter. Neither replaces the other.

---

## Three Forms of Verification

**1. Data verification (ground-truth):** go back to the raw source yourself — not asking Claude to recheck.
"You said Mango Launch ROAS was 8.6x. Check FINAL_v2_USE_THIS_1.csv row by row and confirm."

**2. Text verification (eval gate):** a skeptical subagent reviews the draft.
"@skeptical-cfo — read this founder update and tell me what's wrong with it."

**3. Logic verification:** does the conclusion follow from the data?
"You recommended scaling Mango. Show me exactly which numbers support that recommendation."

---

STOP: Run the eval gate. Ask the skeptical-cfo to read `analysis/july-strategy-brief.md` and aggressively flag anything unsupported by data.

USER: Asks for eval gate

ACTION: Run skeptical-cfo on the July strategy brief. CFO should flag:
- Any recommendation without a cited source
- Any number that isn't cross-referenced to a source file
- Any assumption stated as fact
- The subscription demand point specifically: "14 customers is a signal, not a decision. What's the product economics before we build this?"

Save to `reviews/july-strategy-eval.md`

---

## The FAIL Scenario — This Is the Real Lesson

STOP: Read the eval output. Did the skeptical-cfo flag anything real?

USER: Yes — the subscription recommendation was thin. / The ROAS number didn't cite a source.

[If they found a real flag — this is the moment:]

"Good. This is what FAIL looks like. Now here's what you do with it."

The loop-back:
1. You have new information (CFO flagged subscription recommendation as under-supported)
2. Loop back to Step 1 with that information: "New task — check whether 14 customers is enough signal to recommend building a subscription product. What would we need to see to make this call?"
3. Execute with the corrected constraint
4. Run the eval gate again on the new version
5. If PASS → commit. If FAIL → loop again.

STOP: Loop back. Define the new task based on what the CFO flagged. Re-run the analysis with the corrected scope.

USER: Types new task definition

ACTION: Execute the corrected analysis. Run skeptical-cfo again. If it passes, save the updated brief to `analysis/july-strategy-brief-v2.md`. If it flags something new, loop again.

---

STOP: [CHECKPOINT] What's the difference between the eval gate failing and the analysis being wrong?

USER: Answers

[Whatever they say, land on:] "They're the same thing — the eval gate is just catching it before Vikram does. He would have spotted the unsupported recommendation in the meeting. Your skeptical-cfo spotted it first. That's the whole point."

---

## Commit Only on PASS

The last step matters as much as the first.

Do not save, send, or act on an output until the loop completes with PASS. "It looks right" is not a PASS. A PASS means:
- Eval gate ran and either found nothing, or you fixed what it found
- Key numbers were ground-truthed against the source file
- The output reflects the fixes

STOP: [QUIZ] Your skeptical-cfo flagged two things. You fixed one. The second you decided was "probably fine." What's your verification status?

USER: Answers

[If they say PASS: "No. The loop says: fix what's flagged or explicitly override with a reason. 'Probably fine' is not a reason."]
[If they say it's not done yet: "Correct. Fix the second flag, re-run the eval gate. Then commit."]

---

**Next up:** 4.7 — check from anywhere. Output to Telegram, check on your phone.

STOP: Ready? Type /start-4-7

USER: /start-4-7

---

## Success Criteria
- [ ] Student can name all 5 steps of the Boris loop in order
- [ ] Student understands eval gate ≠ ground-truth (Claude self-check vs external check)
- [ ] Eval gate run on July strategy brief via skeptical-cfo
- [ ] reviews/july-strategy-eval.md created with real CFO flags
- [ ] FAIL scenario experienced — student looped back and re-ran with corrected task
- [ ] Student understands "Commit only on PASS" — not "looks right"
- [ ] Ground-truthing geology metaphor landed
