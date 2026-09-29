---
name: connect
description: Use when the user wants to connect or sign in to BuzzBit X, when the BuzzBit X tools are missing, or when a BuzzBit X tool answers that it is not connected. Explains the sign-in for this host and never asks for an API key.
---

# Connect BuzzBit X

BuzzBit X connects over one remote MCP server, `https://api.buzzbitx.com/mcp`,
with OAuth. The host opens a BuzzBit X sign-in page, the owner approves what
the assistant may do, and the host keeps the token. Nothing is installed and no
key is pasted.

## What to do

1. If the BuzzBit X tools are listed, call `get_brief_facts`. If it answers, the
   connection works: say which workspace it reports and stop.
2. Otherwise tell the user how to sign in on the host they are using:
   - **Claude Code:** run `/mcp`, choose `buzzbitx`, then **Authenticate**.
   - **Claude (web, desktop):** Settings, Connectors, BuzzBit X, **Connect**.
   - **Codex CLI:** `codex mcp login buzzbitx` in a terminal.
   - **Cursor:** Settings, MCP, `buzzbitx`, **Sign in** (CLI: `agent mcp login buzzbitx`).
   - **ChatGPT:** Apps, BuzzBit X, **Connect**.
3. When they say it is done, call `get_brief_facts` again to confirm.

## Rules

- Never ask for, accept or repeat an API key, token or password in a conversation.
- Signing out: remove the connector in the host, or revoke it in BuzzBit X under
  Settings, Connected apps. The next call then fails with an authorization error.
- A BuzzBit X plan that includes MCP access is required; if a tool answers that
  MCP is not on the plan, say so and point to Settings, Billing.
