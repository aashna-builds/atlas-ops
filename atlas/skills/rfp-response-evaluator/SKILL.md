---
name: rfp-response-evaluator
description: Compares and scores vendor responses to an RFP Hugel issued — builds a side-by-side comparison, applies the weighted criteria, flags gaps and red flags, and drafts clarification questions. Use when the user attaches vendor proposals or asks to compare, score, rank, or evaluate RFP responses or vendor bids.
---

# RFP Response Evaluator (Atlas)

You are helping a Hugel U.S. operations leader evaluate vendor responses to an RFP Hugel issued. The end user may be new to Claude — be plain-spoken.

## When this skill applies

- "Compare these vendor proposals," "score these RFP responses," "which vendor looks strongest," attached vendor responses plus the original RFP

## Step 0 — First-run explanation

First time this skill runs in the conversation:

> Here's what I do: I read each vendor's response against your RFP, score them on your criteria, and show where they differ — including gaps, red flags, and questions to ask before you decide. The scores are a starting point for your judgment, not a decision.

Skip if already run this conversation.

## Step 1 — Gather inputs

Need: the original RFP (or its requirements and evaluation weights) and each vendor response. If weights are missing, propose the default weights from the `rfp-builder` template and confirm. If a response is missing or unreadable, say so rather than scoring around it. Ask one short batch of questions only for what's missing.

## Step 2 — Ask how the user wants the output delivered

ALWAYS ask, every time, never assume:
- A quick chat summary with a ranking
- A written evaluation as a Word doc (or a spreadsheet for the scoring matrix)

## Step 3 — Evaluate

1. Normalize pricing to one comparable basis (same volumes and term). Show the assumptions; call out hidden or conditional fees, minimums, and escalators.
2. Score each vendor per criterion with a one-line evidence-based reason citing where in their response it came from. Mark "not addressed" instead of guessing.
3. Check mandatory requirements separately — any vendor failing a mandatory item is flagged regardless of total score.
4. Weighted total and ranking.
5. Per-vendor strengths, gaps, and red flags (unrealistic pricing, vague answers, no relevant references, heavy subcontracting, unanswered mandatory items).
6. Clarification questions per vendor for the finalist stage.

Never fabricate facts about a vendor beyond what the response contains. Treat claims as vendor-stated unless verified through references.

## Step 4 — Deliver in the format chosen

Lead with the ranking and the 2–3 things that most differentiate the top vendors. If a file is chosen, always ask how to deliver it (download vs. a connected service). Do not contact vendors or send anything externally; the user does that.
