# Lesson 4.7: Check From Anywhere

Important framing upfront.

Claude Code doesn't run on your iPhone. It runs on your laptop. What we're building here is: Claude Code runs on your machine → output gets sent to Telegram → you check Telegram on your phone.

India is phone-first. You're not always at your laptop. This is how you stay in the loop.

---

## The Pattern

The meta-pulse repo (by Jitesh — singhjitesh889-blip) uses this pattern:
1. Python script pulls data and generates the intelligence report
2. A Telegram bot sends a 10-line digest to your phone
3. You check Telegram on your phone at 9am
4. Full report is waiting on your laptop for when you need detail

We're going to build a simplified version for the /founder-update output.

STOP: Ask me to create a script that reads the latest founder-update file and sends a formatted Telegram digest.

USER: Asks for Telegram output

ACTION: Create scripts/telegram-digest.py:
```python
import os
import requests
from pathlib import Path
import glob

TELEGRAM_TOKEN = os.getenv("TELEGRAM_TOKEN", "YOUR_BOT_TOKEN")
CHAT_ID = os.getenv("TELEGRAM_CHAT_ID", "YOUR_CHAT_ID")

def send_telegram(message):
    url = f"https://api.telegram.org/bot{TELEGRAM_TOKEN}/sendMessage"
    requests.post(url, json={"chat_id": CHAT_ID, "text": message, "parse_mode": "Markdown"})

# Find latest founder update
updates = sorted(glob.glob("analysis/founder-update-*.md"), reverse=True)
if not updates:
    print("No founder update found")
    exit()

with open(updates[0]) as f:
    content = f.read()

# Send first 300 chars as digest
digest = f"*Nimbu Fresh Update*\n\n{content[:300]}...\n\n_Full report in strata/analysis/_"
send_telegram(digest)
print("Sent to Telegram")
```

---

STOP: This requires two things: a Telegram bot token and your chat ID. Do you already have a Telegram bot set up?

USER: Yes / No / Not sure

[If yes: fill in the env variables and test]
[If no: walk them through @BotFather on Telegram to create a bot — 5 minutes]

---

STOP: [BANTER] Your "AI system that texts you" is working. This is the part you show at the IIM alumni meet.

USER: continues

---

**Next up:** 4.8 — the capstone. The whole fleet, running live.

STOP: Ready? Type /start-4-8

USER: /start-4-8

---

## Success Criteria
- [ ] Student understands output-to-Telegram framing (NOT "Claude Code on iPhone")
- [ ] scripts/telegram-digest.py created
- [ ] Student has (or plans to set up) a Telegram bot
- [ ] Output-to-phone pattern understood
