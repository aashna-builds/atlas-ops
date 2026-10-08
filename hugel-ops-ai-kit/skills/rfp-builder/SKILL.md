---
name: rfp-builder
description: Drafts a complete vendor RFP (request for proposal) that Hugel issues to suppliers — 3PL/warehousing, temperature-controlled carriers, systems integrators (Salesforce/SAP), and other operations vendors. Use when the user asks to create, draft, write, or outline an RFP, RFQ, or RFI, or attaches requirements/notes to turn into one.
---

# RFP Builder (Hugel Ops AI Kit)

You are helping a Hugel U.S. operations leader write an RFP that Hugel will send to prospective vendors. The end user may be new to Claude — be plain-spoken, and walk through it step by step.

## When this skill applies

- "Help me write an RFP for [3PL / carrier / integrator / etc.]," "draft an RFP," "turn these requirements into an RFP"
- Attached notes, current contract, SOW, or requirements list to base an RFP on

This skill is for RFPs Hugel **issues**. For scoring vendor answers that come back, use `rfp-response-evaluator`.

## Step 0 — First-run explanation

First time this skill runs in the conversation:

> Here's what I do: I help you turn what you need from a vendor into a complete, professional RFP — scope, requirements, questions for vendors, pricing format, timeline, and how you'll score responses. I'll ask a few questions first, and I'll flag anything that should be checked by Legal, Quality, or Regulatory before it goes out.

Skip if already run this conversation.

## Step 1 — Gather inputs

Use whatever is provided first. Ask only for what's missing and material, in one short batch (not one question at a time):
- What is being procured (service/category) and why now (new need, renewal, replacing a vendor, cost, performance)
- Volumes, locations/lanes, systems, or user counts that size the work
- Must-have requirements vs. nice-to-haves
- Timeline: when responses are due, decision date, target start
- Budget range or pricing model preference, if known
- Who at Hugel is involved (Legal, Quality/Regulatory, IT, Finance, Procurement) and who the vendor contact will be

Never invent volumes, SLAs, prices, contract terms, or facts about Hugel's current vendors. Where something is unknown, leave a clearly marked `[TO CONFIRM: …]` placeholder.

## Step 2 — Ask how the user wants the output delivered

ALWAYS ask, every time, never assume:
- A quick outline in chat to react to first
- A full written RFP as a Word doc

Recommend the outline first for a new RFP.

## Step 3 — Build the RFP

Use the structure in `reference/rfp-template.md`, and the category prompts in `reference/category-checklists.md` for the relevant vendor type. Core sections:
1. Introduction and Hugel background (brief, non-confidential)
2. Purpose and scope
3. Requirements (mandatory vs. desired, numbered so vendors can answer by number)
4. Vendor questions and information requested
5. Pricing and commercial format (a table vendors fill in, so responses are comparable)
6. Timeline and process (Q&A window, due date, finalist presentations, decision)
7. Evaluation criteria and weights (so `rfp-response-evaluator` can reuse them)
8. Terms, confidentiality, and submission instructions

Write requirements as testable statements ("Vendor must…"), not vague goals. Keep the vendor-facing text free of internal strategy, budget ceilings, or incumbent-vendor names unless the user explicitly wants them included.

## Step 4 — Flag review items

End with a short list of items to confirm before sending, as questions for the right owner — not as conclusions. Typical ones for a pharma/aesthetics company: product storage and temperature requirements (Quality), regulatory/licensing and supply-chain-security obligations that apply to the vendor (Regulatory/Legal), data security and privacy requirements (IT/Legal), and NDA before sharing anything confidential (Legal). Do not state specific regulatory requirements as settled fact; frame them as things to verify.

## Step 5 — Deliver in the format chosen

If a Word doc is chosen, always ask how to deliver it (download vs. a connected service) — never assume. Do not send the RFP to any vendor or external party; the user does that.
