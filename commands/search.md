---
description: "Find government contract opportunities on SAM.gov and Grants.gov. Search by NAICS code, set-aside, agency, keywords, or use your saved company profile."
---

# Search for Government Contract Opportunities

Search SAM.gov, GovWin, and state procurement portals for contract opportunities matching the user's company profile and preferences.

## Workflow

1. Read the user's company profile from `~/TenderB/profile.json` to understand their NAICS codes, set-aside eligibility, target agencies, and capability areas
2. If the user provides specific search criteria, use those. Otherwise, use profile defaults
3. Search for matching opportunities using web search of SAM.gov and relevant portals
4. Present results with urgency indicators (🔴 <7 days, 🟡 7-14 days, 🟢 >14 days)
5. For each result show: title, solicitation number, agency, NAICS, set-aside, deadline, estimated value, contract type
6. Offer to score results against the company profile, analyze solicitation documents, or save as a Scout

## If No Profile Exists

If `~/TenderB/profile.json` doesn't exist, ask the user what they're looking for:
- Industry / NAICS codes
- Set-aside type
- Target agencies (federal, state, local)
- Contract size range
- Geographic preference

Then suggest setting up their profile for future searches.

## MCP Integration

When the `tenderb-govcon-scout` server is connected, this command uses live API data:
- `scout_all` for broad multi-source searches
- `search_contracts` for SAM.gov-specific filtered searches
- `search_grants` for grant opportunities

If the server is not connected, fall back to web search.
