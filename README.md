# BuzzBit X plugin

BuzzBit X is a marketing automation and CRM platform for business owners: email,
WhatsApp, Instagram and Facebook messaging, flows, campaigns, bookings and a
customer data platform. This plugin connects your AI assistant to your own
BuzzBit X workspace so you can ask how the business is doing, draft flows and
campaigns, and hand off sends for your approval, without leaving the chat.

It works in Claude (Claude Code, claude.ai, Claude Desktop), ChatGPT and Codex,
Cursor, Grok Bot and Grok Build. Every host talks to the same remote MCP server.

## What it does

- **Reads** your numbers: revenue, orders, new customers, subscribers, bookings,
  and what is built but not switched on (`get_brief_facts`, `list_unfinished`).
- **Drafts** email flows, campaigns and automations. Every draft arrives
  **switched off**; you turn it on in BuzzBit X.
- **Sends** only within the limits the app enforces. A bulk send never goes out
  on the assistant's say-so: it parks, and you approve it in BuzzBit X.
- Skills included: `brief`, `weekly-review`, `holiday-flows`, `agents`, `connect`.

## What it runs, sends and fetches

The plugin contains no local code. It declares one remote MCP server,
`https://api.buzzbitx.com/mcp` (Streamable HTTP), and the skills above, which are
plain instructions. The host sends your requests to that server over HTTPS and
receives your workspace data back. Nothing is sent anywhere else.

## Connect

1. Install the plugin from your host's plugin directory.
2. The host opens a BuzzBit X sign-in page. Sign in, review the permissions
   (read, write drafts, send with approval) and approve.
3. Ask: "How did my business do this week?"

You need a BuzzBit X account on a plan that includes MCP access.
Setup details for every host: https://www.buzzbitx.com/docs/mcp

To disconnect, remove the connector in your host or revoke it in BuzzBit X
under Settings, Connected apps.

## Privacy Policy

When you use this plugin, your assistant sends your requests to BuzzBit X and
receives your own workspace data back (customers, orders, campaigns, flows,
messages, analytics). BuzzBit X uses that data only to answer the request and
records each tool call in your workspace's audit log. BuzzBit X does not sell
personal information. Account data is kept while your account is active and
erased within 30 days after deletion; server logs are kept for 90 days.
Privacy questions: support@buzzbitx.com.

Full policy: https://www.buzzbitx.com/privacy
Terms: https://www.buzzbitx.com/terms

## Support

support@buzzbitx.com · https://www.buzzbitx.com/support

## License

MIT
