---
name: weekly-review
description: Use for a weekly or monthly review of the business — what moved, what stalled, what to do next. Reads BuzzBit X and may draft; never sends.
---

# Weekly review

Reads, and may leave drafts. Never sends.

## What to do

1. `get_brief_facts` for the current position, and `get_revenue_stats` for the trend.
2. `list_unfinished` — things already built and not switched on are the cheapest wins available, so they come before anything new.
3. `list_flows` and `list_campaigns` to see what is running versus sitting in draft.
4. If the user wants to act on what you found, `create_flow_draft` or `create_campaign_draft`. **Drafts arrive disabled.** Say so — the merchant enables them in BuzzBit X.

## Judgment

Name one thing to fix, not five. A review that lists nine opportunities gets none of them done, and the merchant already knows the business has problems — what they lack is a decision about which one is this week's.

Prefer the constraint earliest in the funnel. Traffic that never converts is not fixed by sending more email at it.

## The one rule that matters

Every number comes from tool output. If you want to say a campaign underperformed, quote what the tool returned; if the tool did not return a benchmark, do not invent one.

## If a tool is not listed

The host shows a small core of BuzzBit X tools. Anything else is reached with `buzzbit_search_tools` (find it by what it does) and then `buzzbit_call_tool` (call it by name). Same limits, same approvals.
