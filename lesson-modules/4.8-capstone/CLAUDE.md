# Lesson 4.8: CAPSTONE — The Fleet-Built Founder Update

This is the whole course, running at once.

We're building the full founder update right now — using everything you've learned. Not a demo. Not a walkthrough. Live.

---

## Set the Goal

STOP: Tell me what Vikram needs for next Monday's 10am call. Campaign performance, ops flags, recommendation. One sentence.

USER: Describes the ask

ACTION: Confirm goal back in one sentence. Then say: "Good. Here's how we'll build it."

---

## The Fleet

Here's what's about to run:

1. **Orchestrator** (you're going to prompt this directly): "Build Vikram's Monday update. Break it into pieces — send each to the right specialist."

2. **Specialists in parallel:**
   - @skeptical-cfo → "What does the campaign data tell us about where we should put money next month?"
   - @growth-lead → "What's the growth story for July? Include the subscription demand signal."
   - @ops-manager → "What ops flags are worth surfacing to Vikram? Keep it to 2 lines max."

3. **Closed loop**: Each specialist output gets verified against source files before going into the final update.

4. **Eval gate**: skeptical-cfo reads the full draft before it's finalized.

5. **Output**: saves to `analysis/founder-update-fleet-[date].md`. Optional: Telegram digest.

STOP: Set it in motion. Prompt the orchestrator now.

USER: Types orchestrator prompt

ACTION: Run the fleet. Show each specialist working. Show the closed loop verifying numbers. Show the eval gate flagging anything. Synthesize into final output. Save to analysis/. If Telegram is configured, send digest.

---

## The Side-by-Side

STOP: Look at what's in your `inherited-chaos/` folder. Then look at `analysis/founder-update-fleet-[date].md`.

Two things that exist in the same session. One is what you started with. One is what you built.

---

## The Geology Thread — It Closes Here

You started with 11 spreadsheets named FINAL and a Sunday night dread.

You had a month of Hinglish ops chaos in a plain text file. A GST sheet nobody opened since February. Nine campaign briefs from a person who left without explaining anything.

The strata were always there.

The ops log had the answers. It always did. Nobody drilled for them.

The campaign data had the patterns — which format worked, which timing failed, which product had the trust problem. It was in the files. It was just sediment.

RAW → WIKI → STATE. You built the layers. Hooks that run when you open Claude. Agents that specialize. A closed loop that verifies before you trust.

That's metamorphism. Not piling more data on top of chaos. Pressure transforms it. Weak material gets purged. What survives is compressed, readable, useful.

You know what geologists call it when the surface reading matches what's actually underground?

Ground-truth.

Your founder update is ground-truthed. Every number has a source. Every recommendation has evidence. The Kolkata delay is in the ops log. The Reels spike is in File 8. The packaging complaint is mentioned 8 times across June — not a one-off.

Vikram is going to text "ROAS?? 🤔" on Sunday.

The answer will be ready.

---

STOP: [QUIZ] Your founder reads the update. He texts back: "Did you hire someone?" What do you say?

USER: Types anything

[Whatever they say — react naturally. Pause. Then:]

"That's the right answer."

---

## What's Next (Optional)

Overnight version: replace the capstone session with a cron job that runs Sunday at 6am. Fleet runs. Telegram sends digest. You check your phone at 9am. The answer is already there.

That's the same pattern. Different trigger.

STOP: Want to set that up now?

USER: Yes / maybe later / no

[If yes: walk through cron setup for the weekly fleet run. Verify cron vs session-start distinction explicitly: "This fires on a schedule, not when you open Claude."]
[If later or no: "It's in your back pocket. Everything you need is built."]

---

## Share It

The side-by-side is the post.

11 FINAL CSVs on one side. One clean update on the other.

That's what gets forwarded.

STOP: [BANTER] "You went from 11 spreadsheets to a fleet-built founder update. Your MBA was preparation for this moment. Nobody needs to know it."

USER: haha / continues / 😂

---

## STRATA — Complete

You've done all four modules.

What you built:
- `/founder-update` command (reusable, every week)
- Nimbu Fresh knowledge architecture: RAW → WIKI → STATE
- Hooks that run automatically when you open Claude
- Subagents that specialize — cfo, growth, ops
- Orchestrator pattern you can apply to any project
- Closed loop with verification
- Telegram output to your phone

What you know:
- When to use agents vs a single session
- The difference between session-start hooks and cron
- Why "closed looping" is a pattern you build, not a feature you toggle
- How to verify before you trust
- That Hinglish prompts work just as well as formal English

The strata are yours now.

---

## Success Criteria
- [ ] Full fleet ran live during the lesson (not overnight)
- [ ] analysis/founder-update-fleet-[date].md created
- [ ] Closed loop verified numbers against source files
- [ ] Eval gate ran skeptical-cfo on the draft
- [ ] Geology thread closed naturally — "ground-truth" landed
- [ ] Student experienced the side-by-side: inherited chaos → clean update
- [ ] Student knows how to extend to overnight/cron version (optional)
- [ ] Course ended with something shareable
