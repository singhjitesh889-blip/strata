# Lesson 1.4: Skills — Your First Slash Command

Before we go faster, let's learn the controls.

This lesson covers the commands, shortcuts, and modes that make Claude Code feel like a power tool instead of a chat window.

[G3: skip to "Build /founder-update" section below if you already know the built-in commands]

STOP: Ready to become a power user?

USER: Yes

---

## Essential Slash Commands

Type `/` to see all available commands. Here are the key ones:

- `/model` — switch between Claude models (Sonnet for speed, Opus for hard thinking)
- `/clear` — start a fresh conversation (context is gone — use carefully)
- `/compact` — compress the conversation to save context space (keeps working, uses less memory)
- `/resume` — pick up exactly where you left off in a previous session
- `/usage` — see how much of your usage limit you've spent

STOP: Type `/` right now to see the command menu. Tell me one command you see that looks interesting.

USER: Names a command

[React to whatever they picked. Explain what it does in one sentence.]

---

## Escape to Interrupt

Here's one that will save you constantly: **Escape to stop me mid-output.**

If I'm running something and you realize I'm going in the wrong direction — hit Escape. I stop. You can correct me. Then we continue.

Let's try it. I'm going to start a long task.

ACTION: Start listing all files recursively from inherited-chaos/ — something that takes a visible moment.

STOP: Hit Escape to interrupt me. Then tell me you did it.

USER: Interrupted you / hit escape

"Exactly. You're in control. Never let me run in the wrong direction just because you didn't want to be rude."

---

## Rewind (Esc × 2)

If Escape stops me mid-task, Esc × 2 gives you a time machine.

It shows you options to undo my recent actions — revert conversation only, or revert conversation AND any files I changed.

STOP: Try it — hit Escape twice. What options do you see?

USER: Describes the rewind options

"Your safety net. Try something risky, rewind if it goes wrong. After you understand this, `--dangerously-skip-permissions` stops feeling dangerous."

---

## Think Keywords

You can tell me how hard to think:
- `"think about X"` — normal
- `"think harder"` — deeper analysis
- `"ultrathink"` — maximum. (You'll see a rainbow. Not a metaphor.)

Use these when my first answer feels too surface-level. Good for: strategic decisions, complex analysis, debugging something unusual.

STOP: Try it — say "ultrathink about which of Nimbu Fresh's 11 campaigns is probably worth looking at first."

USER: Types the ultrathink prompt

ACTION: Think about it with visible extended thinking. Give a genuine answer about which campaigns are likely worth analyzing first based on what we know.

---

## The Three Modes

Claude Code has three input modes. Switch with Shift+Tab:

- **Edit mode** (default) — I ask permission before making changes. Safe, slightly slower.
- **Auto mode** — I just do it. Faster, but you're trusting me more.
- **Plan mode** — I create a plan first, you review it, then I execute. Good for complex multi-step work.

Most people start in Edit mode. Graduate to Auto once you trust the workflow.

---

## --dangerously-skip-permissions

When you start Claude Code normally: `claude`
The power mode: `claude --dangerously-skip-permissions`

No permission prompts. No confirmation dialogs. I just execute.

Called "dangerously" for a reason — you're giving me full control. But when you trust what's happening (and you have git as your undo), it's dramatically faster.

STOP: You now have: interrupt, rewind, three modes, and power mode. Feel different about the terminal?

USER: Reacts

---

## Build Your First Custom Command: /founder-update

Here's the real lesson.

Every time you typed `/start-1-1` or `/start-1-2` — those were custom commands. They live in `.claude/commands/`. Look:

ACTION: Run `ls .claude/commands/` — show all the start commands.

Custom commands are just files with instructions. A shortcut for things you do repeatedly.

We're going to build one right now — `/founder-update`.

Every Monday morning, you'll want a clean summary from all available data for Vikram. Instead of asking every time, you build the command once.

STOP: Ask me to create the `/founder-update` command — it should read all files in analysis/, synthesize them into a one-page update with ROAS, top 3 campaigns, one ops flag, and one recommendation, and save to analysis/founder-update-[date].md.

USER: Asks for the command

ACTION: The /founder-update.md command already exists in .claude/commands/. Show them it's already there. Read it out. Explain what each line does. This is the skill they'll use every week.

"A slash command is like core sampling. You drill once, extract the same reading every time. One command, forever."

STOP: [QUIZ] Where do custom commands live on your computer?

USER: .claude/commands/ / strata folder / somewhere

[Whatever they say, confirm: ".claude/commands/ — that folder is your shortcut library. Any .md file you put there becomes a /command."]

---

**Next up:** 1.5 — does Claude understand Hinglish? Short answer: yes.

STOP: Ready? Type /start-1-5

USER: /start-1-5

---

## Success Criteria
- [ ] Student knows /model, /clear, /compact, /resume
- [ ] Student practiced interrupting with Escape
- [ ] Student saw rewind options (Esc×2)
- [ ] Student knows think/ultrathink keywords
- [ ] Student understands three modes (Edit, Auto, Plan)
- [ ] Student knows about --dangerously-skip-permissions
- [ ] /founder-update command exists and student understands what it does
- [ ] Student ready for 1.5
