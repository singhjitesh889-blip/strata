# Lesson 1.6: 11 Campaigns, One Monday Morning

It's Sunday. Vikram wants ROAS by 10am Monday. You have 11 files.

Normally you'd open them one by one. Read each one. Try to synthesize in your head. That would take most of Sunday night.

Or — you could spin up 11 instances of Claude and process all of them simultaneously.

This is where things get fast.

STOP: Ready to process everything at once?

USER: Yes

---

## The Big Reveal: Parallel Agents

Here's what's about to happen.

I can create multiple instances of myself — agents — and give each one a separate task. They all work at the same time.

Think of it like cloning. I make 11 copies of myself. Each copy gets one CSV file. All 11 work in parallel. Then I combine what they found.

STOP: [QUIZ] When should you use agents? A) One complex task, or B) Many similar tasks?

USER: B / many similar tasks

[If A: "Logical guess. Incorrect. B — parallel, similar tasks. One complex task needs a focused conversation. 11 similar files need a fleet."]
[If B: "Exactly. If you could hand the same instruction to 11 interns and have them each work independently — agents are perfect."]

---

## 11 Files, One Pass

STOP: Ask me to use agents to analyze all 11 CSV files in inherited-chaos/ad-csvs/ and create a campaign ranking report sorted by ROAS. One agent per file. Then synthesize everything into analysis/campaign-ranking-report.md.

USER: Asks for parallel agent analysis

ACTION: Launch 11 agents — one per CSV file. Each agent:
1. Reads its CSV file
2. Normalizes date and number formats
3. Extracts: campaign name, date range, total spend, total revenue, average ROAS, notable flags
4. Returns structured data

Synthesize all 11 into analysis/campaign-ranking-report.md — ranked table by ROAS, with notes on data quality issues.

Key discoveries to surface:
- Mango Launch (Files 1+2): 8.4x average ROAS — top performer
- Reels Ad v2 (File 8): 9.2x on June 7 — spike, reason unknown
- Jeera Lemon (File 3): 3.8x — weak, possible product issue
- Competitor Comparison (File 7): Paused mid-run — legal flag
- Brand Awareness (File 9): Different objective — ROAS comparison not fair

---

STOP: [BANTER] 11 files. Analyzed simultaneously. Done before you finished your chai. ☕

USER: haha / wow / continues

---

## The Cross-Source Analysis

Now let's go deeper. Four specialized agents, each doing something different:

STOP: Ask me to run 4 agents at once: Agent 1 ranks campaigns by ROAS, Agent 2 finds patterns in what made top campaigns work, Agent 3 cross-references with the ops log to see if ops problems hit campaign performance, Agent 4 identifies which campaigns are worth scaling vs killing.

USER: Asks for the 4-agent cross-source analysis

ACTION: Launch 4 specialized agents:
1. Ranks by ROAS from campaign-ranking-report.md
2. Finds patterns: Reels > Static, mobile > desktop, morning creative performing better on spike days
3. Cross-ref: June 7 Kolkata delay correlates with... nothing actually, that's ops, not campaign. But the Reels spike on June 7 was on the SAME day as the Kolkata delay — interesting coincidence, different channels
4. Scale/kill recommendations based on ROAS + trend

Synthesize into analysis/comprehensive-campaign-analysis.md

Surface the key discovery: Mango Launch is the hero. Independence Day worked last year and nobody documented it properly. Competitor Comparison was paused for legal reasons but the 3 days it ran showed strong ROAS — worth pursuing properly.

---

## When to Use Agents (and When Not To)

**Use agents when:**
- Many similar files to process
- Work is parallelizable (each piece can be done independently)
- You need multiple perspectives simultaneously

**Don't use agents when:**
- One complex task that needs back-and-forth
- Sequential work where step 2 depends on step 1
- Things that need to build on each other

STOP: [CHECKPOINT] Quick mental test — which of these is a good use of agents?
A) "Help me think through the best strategy for Independence Day campaign"
B) "Analyze these 5 competitor research files and give me one page on each"

USER: B

[If B: "Right. B is parallel, similar, independent. A is strategic — needs a conversation, not a fleet."]
[If A: "B is the right answer. Five similar files = five agents. Strategic thinking = focused conversation, not a fleet."]

---

**Next up:** 1.7 — the ops log has been sitting there for a month. Someone needs to read it properly. That's you. Kind of.

STOP: Ready? Type /start-1-7

USER: /start-1-7

---

## Success Criteria
- [ ] Student saw 11 agents process campaigns in parallel
- [ ] analysis/campaign-ranking-report.md created with ranked table
- [ ] analysis/comprehensive-campaign-analysis.md created
- [ ] Student knows when to use agents vs not (parallel/similar vs sequential/complex)
- [ ] Key insight surfaced: Mango is the hero, Reels work better than static, legal paused one campaign
- [ ] Student ready for ops log lesson
