# Lesson 2.1: RAW → WIKI → STATE

Remember last session? We built the campaign analysis. The ops intelligence. The founder update.

Now open a new Claude Code session and ask me: "What's Nimbu Fresh's best-performing campaign?"

STOP: Try it — new session, no context. What happens?

USER: I don't know / Claude doesn't know / I'd have to re-explain

"Exactly. I forgot everything. You'd have to re-explain Nimbu Fresh, the 11 CSVs, Vikram, all of it. Every. Single. Session.

That stops today."

---

## The Three Layers

Every professional operation has three types of information. Most people treat them all the same. That's the problem.

**RAW** — raw data. Everything dumped. Your 11 CSVs. Your ops log. Your GST sheet. Messy, recent, unprocessed.

**WIKI** — organized knowledge. Cleaned. Structured. One file per question type. "What are Nimbu Fresh's top campaigns?" → one file answers it.

**STATE** — the briefing doc. What Claude reads every session. ≤800 tokens. The essential read.

In geology, strata are the rock layers that hold the record of everything that happened. RAW is sediment — new deposits every day. WIKI is the geological survey — organized, searchable. STATE is the core sample — the most compressed, essential read.

STOP: [QUIZ] Where does ops-log-june.txt live in this system?

USER: RAW

"Yes. And campaign-ranking-report.md?"

USER: WIKI / it's organized already

"And the STATE? Doesn't exist yet. We build it next lesson."

---

## Map Your Layers

STOP: Let's map Nimbu Fresh. Ask me to help you organize every file we've created so far into RAW, WIKI, or STATE.

USER: Asks for mapping

ACTION: Walk through every file in the strata/ folder:
- inherited-chaos/* → all RAW
- analysis/campaign-ranking-report.md → WIKI
- analysis/ops-intelligence-june.md → WIKI  
- analysis/ops-campaign-correlation.md → WIKI
- analysis/founder-update-jun-2026.md → STATE candidate (or output)
- company-context/* → STATE (already curated)
- progress.md → META (course state, not business state)

Show the mapping. This is their architecture.

---

**Next up:** 2.2 — write the STATE layer. The thing Claude reads before doing anything.

STOP: Ready? Type /start-2-2

USER: /start-2-2

---

## Success Criteria
- [ ] Student experienced the "blank session" problem firsthand
- [ ] Student understands RAW / WIKI / STATE distinction
- [ ] Every existing file mapped to its layer
- [ ] Geology metaphor introduced (stratigraphy) — naturally, not announced
- [ ] Student motivated to build the STATE layer
