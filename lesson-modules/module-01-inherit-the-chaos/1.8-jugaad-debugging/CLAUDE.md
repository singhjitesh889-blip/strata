# Lesson 1.8: When It Breaks

Claude will get something wrong. Guaranteed.

This lesson is about what to do when that happens — quickly and correctly.

STOP: Has Claude given you a wrong or confusing output yet in this course?

USER: Yes / No / Kind of

[If yes: "Good. Let's use that."]
[If no: "We'll manufacture one right now."]

---

## The Three Types of Wrong

**Type 1 — Wrong data:** Claude made a number up or misread a file.
*How to fix:* Point to the specific error. "You said 8 campaigns ran in June. The ops log says there were 9 campaign briefs in old-campaigns/. Re-check campaign-3-monsoon-detox.txt."

**Type 2 — Wrong interpretation:** Claude answered a different question than you asked.
*How to fix:* Be more specific. This usually means YOUR prompt was ambiguous. Add a rule to CLAUDE.md so it doesn't happen again.

**Type 3 — Wrong format:** The content is right but the presentation is wrong.
*How to fix:* Ask for a different format. "Give me this as a table, not paragraphs."

STOP: [QUIZ] You asked me to find the average ROAS across all 11 campaigns. I gave you one number. What's your first move before using it?

USER: Check / verify / look at the source / open the file

[If verify: "Yes. Open campaign-ranking-report.md and spot-check 2-3 numbers. If they match what I said, trust the rest."]
[If use it: "Brave. But wrong. One spot-check takes 30 seconds. A wrong number in a Vikram slide takes much longer to explain."]

---

## The CLAUDE.md Fix

Here's the most important thing in this lesson.

When Claude makes the same mistake twice — that's a CLAUDE.md problem, not a Claude problem.

**Every recurring mistake → add a rule. Not "fix it this time" → "make sure this never happens again."**

This is the difference between a one-time patch and a system that gets smarter.

STOP: Ask me to add a rule to CLAUDE.md about something you've noticed or something you want me to always do differently when working on Nimbu Fresh.

USER: Names a rule they want — e.g., "always cite sources," "always show data as tables," "remind me to verify numbers," etc.

ACTION: Check if CLAUDE.md exists at the project root. If not, create it. Add the rule they asked for in clean, clear language. Show what was added.

[After adding:] "That rule now applies to every session in this folder. This is how you build a Claude that knows your preferences — not by correcting it every time, but by encoding the correction as a rule."

---

## Fast Patch vs Root Fix

Sometimes you need the answer NOW and the fix can wait. That's fine — just know which you're doing.

**Fast patch:** "For now, just give me the top 3 campaigns by ROAS. I'll verify later."

**Root fix:** "Add a rule to CLAUDE.md: always sort campaign data by ROAS descending. Always cite which file the number came from."

Both are valid. The mistake is doing a fast patch and thinking you've done a root fix.

STOP: [BANTER] "Fix it this time" is how the previous Growth Lead operated. Look where they are now.

USER: haha / continues

---

**Next up:** 1.9 — the 9 PM founder update. This is what the whole module has been building toward.

STOP: Ready? Type /start-1-9

USER: /start-1-9

---

## Success Criteria
- [ ] Student knows the 3 types of wrong (data / interpretation / format)
- [ ] Student has added at least one rule to CLAUDE.md
- [ ] Student understands fast patch vs root fix distinction
- [ ] "Write rules, not corrections" principle introduced (deepens in M2.5)
- [ ] Student ready for the capstone of Module 1
