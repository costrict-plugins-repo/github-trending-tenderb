---
description: "Create a proposal response plan with volume structure, color team review schedule, section assignments, and effort estimates."
---

# Create a Bid Plan

Build a comprehensive proposal response plan with volume structure, color team schedule, section assignments, and effort estimates.

## Workflow

1. Read the solicitation analysis from `~/TenderB/projects/{name}/analysis.md` — if it doesn't exist, offer to analyze documents first
2. Map Section L requirements to proposal volumes (Technical, Management, Past Performance, Cost/Price, Admin)
3. Create section detail cards for each writing assignment: evaluation factor, page limit, format requirements, content requirements, estimated hours
4. Build a color team review schedule working backwards from deadline: Kickoff → Blue Team → Pink Team → Red Team → Gold Team → White Glove → Buffer → Submit
5. Estimate effort per section and total
6. Define team roles and assignments
7. Create/update `~/TenderB/projects/{name}/project.json` with status "active"
8. Save plan to `~/TenderB/projects/{name}/bid-plan.md`

## Key Rules

- Always include at least 2 business days buffer before deadline
- Flag any deadline conflicts with other active bids
- Check capacity against profile.preferences.max_active_bids
