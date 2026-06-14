# Lesson 1.3: Cleaning Without Excel Formulas

You've seen the mess. Now let's do something about one piece of it.

We're going to clean `FINAL_v2_USE_THIS_1.csv` — the Mango Launch campaign data.

Without Excel. Without formulas. Just by asking.

STOP: Ask me to read FINAL_v2_USE_THIS_1.csv and tell you everything that's wrong with it.

USER: Asks Claude to analyze the CSV

ACTION: Read the file. Identify and explain every data quality issue:
- Date column has 4 different formats (1/6/2026, 04-Jun-26, Jun 6, 7/6/2026)
- June 3 row: Spend, Purchases, and ROAS are missing
- Revenue column says "Revenue(INR)" but File 2 uses "rev_inr" — different column names for same data
- Numbers in File 1 and File 2 (covering the same campaign) don't match exactly
Explain each problem clearly, without jargon.

---

STOP: [QUIZ] Why does it matter that Date formats are inconsistent?

USER: Answers — sorting won't work / can't compare / Excel breaks / etc.

[If correct direction: "Exactly. You can't sort, filter, or aggregate dates if they're stored as text in three different formats."]
[If off: "Here's why: if you try to sort by date, Jun 6 and 1/6/2026 don't sort together. The computer sees them as different types of data, not the same date. Chaos in → chaos out."]

---

STOP: Ask me to create a clean, normalized version of this file — standardize all dates to YYYY-MM-DD, fill the missing June 3 spend with BLANK, remove the duplicate rows, rename columns to a consistent format, and save it to analysis/FINAL_v2_USE_THIS_1_CLEAN.csv.

USER: Asks Claude to clean the file

ACTION: Create analysis/FINAL_v2_USE_THIS_1_CLEAN.csv with:
- Dates normalized to YYYY-MM-DD
- Missing values marked as BLANK
- Consistent column names: campaign_name, date, spend_inr, impressions, clicks, purchases, revenue_inr, roas, notes
- Any duplicate rows removed

---

## The Most Important Part

Before you use this file for anything, you should check my work.

STOP: Look at the cleaned file. Does it look right to you? Any number that seems off?

USER: Reviews it / says it looks good / flags something

[If they flag something: "Good catch. Let's fix that." Fix it.]
[If it looks fine: "Good. This is the habit — verify before you trust. I can make mistakes. You're the final check."]

This is rule one of working with Claude Code on data: **verify before trusting.** I will occasionally misread a number, misparse a format, or make an assumption. You catch it by looking.

STOP: [CHECKPOINT] 10 more CSVs are still messy. But you just learned the move. What would you do differently when cleaning FINAL_v2_USE_THIS_2.csv — knowing what we just found in File 1?

USER: Answers

[React naturally. The answer doesn't matter — the habit of thinking-before-acting does.]

---

**Next up:** 1.4 — commands that make everything faster. Including how to build your own.

STOP: Ready? Type /start-1-4

USER: /start-1-4

---

## Success Criteria
- [ ] Student saw all data quality issues in File 1 explained clearly
- [ ] analysis/FINAL_v2_USE_THIS_1_CLEAN.csv created
- [ ] Student practiced verifying Claude's output before trusting it
- [ ] "Verify before trust" habit explicitly named
- [ ] Student ready for commands lesson
