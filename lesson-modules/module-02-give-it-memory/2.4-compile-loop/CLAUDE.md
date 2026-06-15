# Lesson 2.4: The Compile Loop

Here's the trap most people fall into.

They build their WIKI files. They add to them. Every month, more rows. More notes. The files get longer. "My system is getting better," they think.

It's not. It's getting heavier.

---

## Metamorphism, Not Sedimentation

In geology, there are two ways sediment gets transformed.

**Sedimentation:** layers pile up. More and more material added on top. Gets heavy. Eventually compresses under its own weight.

**Metamorphism:** heat and pressure transform the existing material. The original structure is rewritten into something denser, stronger. Weak material is purged. What survives is fundamentally changed.

The compile loop is metamorphism.

Every month: you don't ADD to your WIKI files — you REWRITE them. New data comes in, old patterns get validated or killed, the file that comes out is not "last month's + new stuff" — it's a rewrite incorporating everything you now know.

STOP: [QUIZ] Your ops WIKI file from June has 8 packaging complaints. In July the problem is fixed — zero complaints. Do you: A) Add a "July: 0 complaints" row, or B) Rewrite the packaging section to reflect resolved status?

USER: B

[If B: "Exactly. B. You rewrite it to say 'Packaging complaint: resolved June 22 with new cap batch. Monitor through Q3.' The 8 incidents are context — not a growing list."]
[If A: "A adds weight. B adds clarity. The question is: what does Claude need to know NOW? Not: what happened historically. That's what the raw data is for."]

---

STOP: Let's practice. Ask me to take the ops-intelligence-june.md and rewrite it as a clean current-state WIKI entry — not a list of June incidents, but a statement of current ops posture with historical context compressed into one line where relevant.

USER: Asks for rewrite

ACTION: Create analysis/wiki-ops-current.md — not a log, but a current-state document:
- Current stock status (from last known data)
- Packaging: resolved, monitoring
- Courier: Lucknow resolved, Delhivery performing
- Demand signals: subscription interest (14 customers June), Kokum organic growth
- Next actions: Independence Day plan by Aug 1, courier alternative evaluation (Xpressbees quote received)

---

STOP: Compare wiki-ops-current.md to ops-intelligence-june.md. Which would you rather Claude read before helping you plan July?

USER: wiki-ops-current / the new one

"The compile loop. You just ran it. New data in, WIKI rewritten, weak material purged."

---

**Next up:** 2.5 — write rules, not corrections. The habit that makes everything compound.

STOP: Ready? Type /start-2-5

USER: /start-2-5

---

## Success Criteria
- [ ] Student understands rewrite vs append distinction (metamorphism metaphor)
- [ ] analysis/wiki-ops-current.md created (rewritten, not appended)
- [ ] Student experienced the difference between a log and a current-state document
- [ ] Ready for write-rules lesson
