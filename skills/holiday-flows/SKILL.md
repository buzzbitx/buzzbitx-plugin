---
name: holiday-flows
description: Use when the user wants to prepare for an upcoming holiday or seasonal moment — drafts email flows and campaigns for it. Creates disabled drafts only; never sends.
---

# Holiday flows

Creates drafts. Every one arrives **disabled**. Nothing here sends.

## What to do

1. `get_brief_facts` — it reports holidays already inside their lead window, so you do not have to guess which is next or how long there is.
2. `search_platform_knowledge` for the workspace's own voice, offers and policies before writing any copy. Generic holiday copy is the thing merchants most reliably delete.
3. `create_flow_draft` — three of them, and make them genuinely different: an announcement, a reminder with a reason to act, and a last-chance. Three variations of the same email is one email.
4. Tell the user plainly: three drafts, all disabled, here is where to review them.

## What not to do

Do not call `send_campaign`. If the user asks you to send, that is a bulk send: it will park for their confirmation and they will approve it in BuzzBit X. Say that rather than trying and reporting a failure.

Do not invent a discount. A percentage the merchant did not authorise is a real cost, and the draft is likelier to be sent than corrected.

## The one rule that matters

Prices, product names and policies come from tool output — `search_platform_knowledge` or the catalog — never from what seems plausible for this kind of business.

## If a tool is not listed

The host shows a small core of BuzzBit X tools. Anything else is reached with `buzzbit_search_tools` (find it by what it does) and then `buzzbit_call_tool` (call it by name). Same limits, same approvals.
