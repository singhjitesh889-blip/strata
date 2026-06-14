# Lesson 4.1: MCP Setup — The Hard Part First

MCP stands for Model Context Protocol.

In plain language: it gives Claude Code live connections to real systems. Not files you load manually — actual backends, APIs, databases, queried in real time.

In geology: MCP is a seismograph. It gives Claude senses it doesn't have natively — the ability to detect what's happening underground without needing to drill a new hole every time.

This lesson is dedicated to setup because this is where non-developers drop off. We're not going to let that happen.

[G3: if you have Node.js 18+ installed — skip to "Configure Claude Code" section]

---

## What We're Installing

`mcp-commerce-starter` by Jitesh Kumar Singh — 1,134 lines, 22 tools. A real commerce backend MCP, not a tutorial toy.

Tools include: order management, inventory, fulfillment, logistics, customer data.

For Nimbu Fresh, this means: Claude can query orders, check stock levels, and pull fulfillment status without you loading files manually.

STOP: Let's check if Node.js is installed. Ask me to run `node --version`.

USER: Asks / types the command

ACTION: Run node --version. If v18+: proceed. If not installed: guide through installation (brew install node on Mac, sudo apt install nodejs on Linux/WSL). Don't proceed until node --version shows v18+.

---

## Clone and Install

STOP: Ask me to clone the mcp-commerce-starter repo and install it.

USER: Asks

ACTION:
```bash
cd ~/Desktop/PersonalProjects
git clone https://github.com/singhjitesh889-blip/mcp-commerce-starter.git
cd mcp-commerce-starter
npm install
```
Show output. If any errors appear, troubleshoot before continuing.

---

## Configure Claude Code

STOP: Ask me to configure Claude Code to use the MCP server.

USER: Asks

ACTION: Create or update ~/.claude/claude_desktop_config.json:
```json
{
  "mcpServers": {
    "nimbu-commerce": {
      "command": "node",
      "args": ["path/to/mcp-commerce-starter/index.js"],
      "env": {}
    }
  }
}
```
Note: Replace path with actual path. Explain: "This tells Claude Code that every session, this MCP server is available as a set of tools."

Restart Claude Code. Verify: /mcp command should now show nimbu-commerce tools.

---

## Top 5 Failure Modes

If something went wrong, here's where to look:

1. **"command not found: node"** → Node.js not installed. Back to first section.
2. **"cannot find module"** → npm install didn't complete. Run again.
3. **Claude doesn't see MCP tools** → Claude Code needs a full restart after config changes.
4. **Config file not found** → Create it at `~/.claude/claude_desktop_config.json` — it may not exist yet.
5. **MCP server crashes immediately** → Run `node index.js` in a separate terminal to see the error.

STOP: Is the MCP server showing in Claude Code? Type /mcp to check.

USER: Yes it's there / No / I see an error

[If yes: proceed to 4.2]
[If no: troubleshoot using the failure modes above]

---

**Next up:** 4.2 — wire it and ask in Hinglish.

STOP: Ready? Type /start-4-2

USER: /start-4-2

---

## Success Criteria
- [ ] Node.js v18+ confirmed installed
- [ ] mcp-commerce-starter cloned and npm install complete
- [ ] claude_desktop_config.json configured
- [ ] Claude Code restarted and MCP tools visible
- [ ] Student ready to query via MCP
