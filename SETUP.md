# STRATA — Getting Started
*The first Claude Code course built for Indian knowledge workers.*

**Before the course begins, you need 4 things:**
1. A terminal (the black window where you type commands)
2. Node.js (runs JavaScript — needed to install Claude Code)
3. Claude Code (the tool this entire course runs inside)
4. A Claude subscription (or API key)

This takes about 15 minutes. Every step is below. No step is skipped.

---

## Step 1 — Open a Terminal

**Mac:**
Press `Cmd + Space` → type "Terminal" → press Enter.
A dark window opens with a blinking cursor. That is the terminal. You're already halfway there.

**Windows:**
You need WSL2 (Windows Subsystem for Linux — a Linux terminal inside Windows).
Open PowerShell as Administrator (search "PowerShell" → right-click → Run as Administrator) and run:
```
wsl --install
```
Restart your computer. Then search for "Ubuntu" in Start Menu and open it. That is your terminal.

**Linux:**
You already have a terminal. Ctrl+Alt+T on most distros.

---

## Step 2 — Install Node.js

Node.js is required to install Claude Code. It runs JavaScript on your computer.

**Mac:**
First install Homebrew (a package manager for Mac):
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
Follow the prompts. Then:
```bash
brew install node
```
Verify it worked:
```bash
node --version
```
Should print `v18.0.0` or higher.

**Windows (WSL) / Linux:**
```bash
sudo apt update && sudo apt install nodejs npm -y
node --version
```

---

## Step 3 — Install Claude Code

In your terminal:
```bash
npm install -g @anthropic-ai/claude-code
```
Verify:
```bash
claude --version
```
Should print a version number. If you see `command not found`, close and reopen your terminal, then try again.

---

## Step 4 — Get Claude Access

**Path A — Claude Max (recommended for beginners, ~₹1,700/month):**
Go to https://claude.ai → sign up → subscribe to Max plan.
Then in your terminal:
```bash
claude
```
Claude Code will open and ask you to sign in. Follow the browser prompt. Done.

**Path B — API Key (pay-as-you-go):**
Go to https://console.anthropic.com → API Keys → Create Key.
Copy the key (starts with `sk-ant-...`).
```bash
export ANTHROPIC_API_KEY=sk-ant-your-key-here
```
To make this permanent:
```bash
echo 'export ANTHROPIC_API_KEY=sk-ant-your-key-here' >> ~/.zshrc
source ~/.zshrc
```
On WSL/Linux replace `~/.zshrc` with `~/.bashrc`.

---

## Step 5 — Get the Course

Make sure git is installed:
```bash
git --version
```
If not: `brew install git` (Mac) or `sudo apt install git` (WSL/Linux).

Clone the course:
```bash
git clone https://github.com/singhjitesh889-blip/strata.git
cd strata
```

---

## Step 6 — Start the Course

```bash
claude
```

Claude Code opens. Type:
```
/start-0
```

The course begins.

---

## Troubleshooting

| Error | Fix |
|-------|-----|
| `command not found: claude` | Run `source ~/.zshrc` then try again |
| `permission denied` on npm install | Run `sudo npm install -g @anthropic-ai/claude-code` |
| `ANTHROPIC_API_KEY not set` | Complete Step 4 above |
| `/start-0 not recognized` | Make sure you're inside the `strata/` folder. Run `cd strata` then `claude` |
| WSL: `node not found` after install | Close Ubuntu window, reopen, try again |
| Claude Code hangs on auth | Run `claude auth logout` then `claude auth login` |

---

*Built by Jitesh Kumar Singh — https://singhjitesh889-blip.vercel.app*
*Course repo: https://github.com/singhjitesh889-blip/strata*
