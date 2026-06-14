---
description: Generate a clean, source-verified founder update from all analysis files
---
Check which files exist in @analysis/. Read all that are present (campaign-ranking-report.md, ops-intelligence-june.md, ops-campaign-correlation.md, and any others). Synthesize into a clean, one-page founder update:

**Format:**
📊 **ROAS This Week:** [number] (source: [file])
🏆 **Top 3 Campaigns:** [name — ROAS — one line on why it worked]
⚠️ **Ops Flag:** [one thing worth knowing, from ops-intelligence]
→ **Recommendation:** [one action, no more]

Rules:
- Every number must be source-cited in brackets after it
- Tone: founder-ready. He will not read more than this.
- If analysis files are missing, say which ones and what data would complete the picture

Save to analysis/founder-update-[today's date].md. Show the output in full.
