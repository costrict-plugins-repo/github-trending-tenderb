---
description: "Run a bid/no-bid qualification on a government contract opportunity. Scores against your company profile using 7 weighted factors."
---

# Score an Opportunity — Bid/No-Bid Decision

Run a 7-factor qualification analysis on a specific opportunity to determine whether to bid.

## Workflow

1. Identify the opportunity — the user may provide a solicitation number, title, URL, or uploaded documents
2. Read the company profile from `~/TenderB/profile.json`
3. Gather opportunity details from available sources (search results, uploaded PDFs, conversation context)
4. Score across 7 factors: NAICS alignment (25%), keyword match (20%), past performance relevance (15%), geographic fit (10%), set-aside eligibility (10%), competitive position (10%), deadline feasibility (10%)
5. Check current capacity: count active bids in `~/TenderB/projects/*/project.json`, compare to max_active_bids
6. Present scorecard with rating (🟢 80+ Strong / 🟢 70-79 Good / 🟡 50-69 Moderate / 🔴 30-49 Weak / 🔴 <30 Poor)
7. Include strategic considerations: incumbent analysis, competition level, teaming potential, strategic value
8. Provide clear Bid/No-Bid recommendation with reasoning

## After Scoring

- If Bid → offer to create a capture plan
- If No-Bid → offer to search for better-fitting opportunities
- If Undecided → offer to analyze the solicitation documents first

## MCP Integration

Uses `get_contract_detail` for full solicitation data and `search_awards` for incumbent analysis when the `tenderb-govcon-scout` server is connected.
