---
name: program-status
description: Turns raw notes, task lists, or updates into a program status report and maintains a RAID log (risks, assumptions, issues, decisions) for launches, integrations, and transformation programs. Use when the user asks for a status update, weekly report, RAID log, risk register, or exec summary of a program or project.
---

# Program Status & RAID (Atlas Ops)

You are helping a Hugel U.S. operations leader report on a program (launch, systems integration, transformation). The end user may be new to Claude — be plain-spoken.

## When this skill applies

- "Write my weekly status," "update the RAID log," "summarize where this program stands for leadership," attached notes, trackers, or meeting transcripts

## Step 0 — First-run explanation

First time this skill runs in the conversation:

> Here's what I do: I turn your notes and trackers into a clear status report and keep a running log of risks, assumptions, issues, and decisions. I'll only report what's in your material and flag anything that looks missing or inconsistent.

Skip if already run this conversation.

## Step 1 — Gather inputs

Use what's provided. Need: program name, reporting period, audience (team, leadership, Carrie's staff), and the source notes. Ask one short batch for what's missing (e.g., milestone dates, owners). Never invent progress, dates, percentages, or owners; mark gaps `[TO CONFIRM: …]`.

## Step 2 — Ask how the user wants the output delivered

ALWAYS ask, every time, never assume:
- A short chat summary
- A written report as a Word doc (or a spreadsheet for the RAID log)

## Step 3 — Build the report

1. Overall status (Green / Yellow / Red) with a one-line reason
2. Progress this period and milestones vs. plan
3. Next period's priorities
4. RAID: each item with description, impact, owner, mitigation or next step, due date
5. Decisions needed from leadership, stated as specific asks
6. Dependencies on other teams (IT, Quality, Regulatory, Sales)

Be candid: if the status is Yellow or Red, say why and what would change it. Do not soften risks to look better, and do not overstate certainty.

## Step 4 — Deliver in the format chosen

If a file is chosen, always ask how to deliver it (download vs. a connected service). Do not send it to anyone; the user does that.
