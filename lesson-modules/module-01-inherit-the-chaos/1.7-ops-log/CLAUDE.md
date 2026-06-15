# Lesson 1.7: What the Ops Log Actually Says

200 lines. One month. Hinglish. Written every day by the ops team.

Nobody read it.

You could read it. Or you could ask.

STOP: Ask me to read ops-log-june.txt and tell you what's actually happening — the recurring problems, inventory alerts, customer complaints worth escalating, and one thing the ops team is stressed about that nobody has named yet.

USER: Types request

ACTION: Read ops-log-june.txt completely. Extract and organize:

**Recurring Problems (with frequency):**
- Packaging complaint: Mango 300ml cap loose/leaking — 8 incidents across month. Escalating. BlueDart Pune route initially, then national. New caps ordered June 22.
- Lucknow hub delays: 3 separate incidents (June 1, June 12, June 19). Different reasons each time. Resolved June 21.
- COD return rate: 3-4% average, with spike week 1 (4.5%)

**Inventory Alerts:**
- Kokum Cooler: 78 units at month-end (LOW)
- Mixed Fruit 1L: CRITICAL June 5 (50 units), emergency restock June 12
- Aam Panna 1L: Out of stock June 14 (seasonal — expected)
- Jeera Lemon: Low early June, restocked June 10

**Customer Escalation:**
- Anjali Sharma #NF-2847: 2 complaints in 2 weeks, wants full refund — escalate to Vikram
- 14 customers asked about subscriptions this month — not a product yet, real demand signal

**The unnamed stress:** "Nobody is reading this log." Written literally on June 25 and June 30 by the ops team. They've been documenting for a month into the void.

Save to analysis/ops-intelligence-june.md

---

## The Aha Moment

STOP: Read that file. What did you notice that you didn't expect?

USER: Comments on something — packaging complaints, subscription demand, the "nobody reading this" note, etc.

[React specifically to what they noticed.]

"The ops log had the answers the whole time. The packaging complaint was raised 8 times across June. That's not a one-off complaint — that's a supply chain failure happening slowly in plain sight. It was in the text file. Nobody compiled it."

---

## Cross-Reference

Now let's connect the data.

STOP: Ask me to cross-reference the ops-intelligence with the campaign-ranking-report. Did ops problems correlate with any campaign underperformance?

USER: Types the cross-reference request

ACTION: Cross-reference ops-intelligence-june.md with campaign-ranking-report.md.

Findings:
- June 7 Kolkata weather delay: 18 orders stuck, but Reels ad ROAS was 9.2x that same day — ops problem and ad spike happened simultaneously. No causal link but worth noting they're independent channels.
- Jeera Lemon packaging complaints in March → contributed to slow Jeera Lemon campaign performance in April/May (brand trust issue, not just the relaunch timing)
- June 1-3: Lucknow delay week overlaps with slightly lower Mango campaign conversion on those same days — possible: customers who got delayed orders didn't convert on remarketing

Save to analysis/ops-campaign-correlation.md

---

## The Bigger Skill

STOP: [CHECKPOINT] What's the difference between asking me to "summarize" the ops log vs "extract structured intelligence" from it?

USER: Answers

[React to their answer — any direction is fine. Then:] "Summarize = shorter version of the same thing. Structured extraction = answer a specific question the data already contains. One is compression. The other is mining."

---

**Next up:** 1.8 — what to do when Claude gets something wrong. Because it will.

STOP: Ready? Type /start-1-8

USER: /start-1-8

---

## Success Criteria
- [ ] analysis/ops-intelligence-june.md created with structured extraction
- [ ] analysis/ops-campaign-correlation.md created
- [ ] Student understood "extract vs summarize" distinction
- [ ] Subscription demand signal surfaced (14 customers this month)
- [ ] Packaging complaint pattern surfaced (8 incidents, escalating, resolved)
- [ ] Aha moment: the data was all there, nobody compiled it
