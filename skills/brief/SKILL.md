---
name: brief
description: Use when the user asks how the business is doing, what happened yesterday or last week, what is unfinished, or asks for the morning brief. Reads BuzzBit X and reports; never sends anything.
---

# Today's brief

Read-only. Nothing in this skill sends, drafts or changes anything.

## What to do

1. Call `get_brief_facts`. It returns the numbers already computed — revenue over 7 and 30 days against the prior period, orders, new customers, subscribers, today's bookings, holidays inside their lead window, and anything unfinished.
2. Call `list_unfinished` if the user asks specifically what is outstanding.
3. Report what came back.

## The one rule that matters

**Every number you say must appear in the tool output.** Do not compute a percentage the fact sheet did not give you, do not annualise, do not estimate a figure that is missing. If something is absent, say it is not available and why — the fact sheet says so itself for metrics that depend on data the workspace has not connected.

The reason is not pedantry. A merchant who catches one invented number stops trusting every real one.

## Shape of a good answer

Lead with the number that changed most. Two or three sentences. Then the unfinished items as a short list, each with what it is and what enabling it would do — not a lecture.

Do not open with a greeting or a preamble about what you are about to do.

## If a tool is not listed

The host shows a small core of BuzzBit X tools. Anything else is reached with `buzzbit_search_tools` (find it by what it does) and then `buzzbit_call_tool` (call it by name). Same limits, same approvals.
