# Lesson 4.4: The Orchestrator Pattern

Let's be clear about something upfront.

The orchestrator pattern is not a Claude Code feature you install or toggle. It's a way you structure your prompt. You design it. You build it.

---

## The Pattern

**Without orchestrator:** You think through all the pieces, write one big prompt, hope Claude handles all of them.

**With orchestrator:** You give Claude one goal. Claude's first job is to break it into pieces, assign each piece to the right specialist, and then synthesize the results.

In geology: one goal is a major tectonic force. The orchestrator is the master fault line. The specialists are the branch faults — each handling a piece of the stress, each working independently.

STOP: Let's build one. The goal: create a July strategy brief for Nimbu Fresh. Ask me to orchestrate this — breaking it into what the CFO needs to see, what the growth lead should plan, what ops should prepare, and what campaigns should run.

USER: Asks for orchestrated July strategy

ACTION: Orchestrate the request:
1. @skeptical-cfo: "Review June performance and identify the top 3 financial priorities for July. Be specific about which campaigns to fund and why."
2. @growth-lead: "Based on June performance, what are the top 3 growth moves for July? Include the subscription demand signal (14 customers in June)."
3. @ops-manager: "What ops preparations are needed for July? Include packaging monitoring, courier status, and stock alerts."
4. Then synthesize into analysis/july-strategy-brief.md with all three perspectives integrated.

---

STOP: [QUIZ] Is the orchestrator a Claude Code feature you can install, or a pattern you build in your prompt?

USER: Pattern / prompt / I build it

[If pattern: "Yes. Claude Code doesn't have an 'orchestrator mode.' You structure the prompt, define the specialists, and let Claude coordinate."]
[If feature: "It's a pattern — not a named Claude Code feature. You design it. Same result, more honest framing."]

---

**Next up:** 4.5 — agentic loops. The machine that reruns.

STOP: Ready? Type /start-4-5

USER: /start-4-5

---

## Success Criteria
- [ ] Student understands orchestrator = pattern, not named feature
- [ ] analysis/july-strategy-brief.md created via orchestrated subagents
- [ ] Student can build the pattern themselves
