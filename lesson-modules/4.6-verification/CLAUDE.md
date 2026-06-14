# Lesson 4.6: Verification + Eval Gate

Here's the highest-leverage habit in this entire course.

Give Claude a way to check its own output.

That single change produces 2-3x better quality on anything involving data.

---

## Ground-Truthing

In geology: before relying on a surface reading, geologists drill to verify — ground-truthing. The surface can be misleading. The drill tells you what's actually there.

Verification in Claude Code is the same idea. Before using an output, verify it against the source.

---

## Three Forms of Verification

**1. Data verification:** re-run the numbers from the source.
"You gave me the ROAS for Mango Launch. Recalculate it from FINAL_v2_USE_THIS_1.csv and confirm."

**2. Text verification:** a skeptical subagent reviews the draft.
"@skeptical-cfo — read this founder update and tell me what's wrong with it."

**3. Logic verification:** does the conclusion follow from the data?
"You recommended scaling Mango. Show me exactly which numbers support that recommendation."

STOP: Run the eval gate. Ask the skeptical-cfo to read analysis/july-strategy-brief.md and aggressively flag anything unsupported by data.

USER: Asks for eval gate

ACTION: Run skeptical-cfo on the July strategy brief. CFO should flag:
- Any recommendation without a cited source
- Any number that isn't cross-referenced
- Any assumption stated as fact
- The subscription demand point: "14 customers is a signal but not a decision. What's the product economics before we build this?"

Save to reviews/july-strategy-eval.md

---

STOP: [CHECKPOINT] Why run a skeptical reviewer on your own output before sending it to Vikram?

USER: Catches errors / finds what I missed / makes it stronger

"Yes. And specifically: Vikram will run this filter himself when he reads it. Better for your skeptical-cfo to catch it first."

---

**Next up:** 4.7 — check from anywhere. Output to Telegram, check on your phone.

STOP: Ready? Type /start-4-7

USER: /start-4-7

---

## Success Criteria
- [ ] Student understands 3 forms of verification (data / text / logic)
- [ ] Eval gate run on July strategy brief
- [ ] reviews/july-strategy-eval.md created with CFO flags
- [ ] Ground-truthing geology metaphor landed
