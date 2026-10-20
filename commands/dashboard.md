---
description: "View your bid pipeline — active proposals, upcoming deadlines, capacity, and win/loss metrics."
---

# Pipeline Dashboard

Show a complete overview of all active bids, upcoming deadlines, capacity status, and performance metrics.

## Workflow

1. Read all project files from `~/TenderB/projects/*/project.json`
2. Read capacity limits from `~/TenderB/profile.json`
3. Read historical performance from `~/TenderB/history.json`
4. Present dashboard organized by urgency:

### Sections to Show

**🔴 Due This Week** — Projects with deadlines in the next 7 days
**🟡 Due Next 2 Weeks** — Deadlines in 7-14 days
**🟢 Due Later** — Deadlines beyond 14 days
**⏳ Submitted — Awaiting Decision** — Bids submitted, pending award

For each project: name, agency, deadline, current status, qualification score

### Capacity Check
- Active proposals: X / Y max
- Deadline conflicts (two deadlines within 5 days)
- Recommendation if over capacity

### Performance Metrics (from history.json)
- Win rate (all time and trailing 12 months)
- Revenue won (trailing 12 months)
- Total bids submitted
- Average qualification score at Go decision

### Active Scouts
- List saved searches from `~/TenderB/scouts/*.json`
- Last run date for each

## If No Data

If no projects exist yet, guide the user to set up their profile and start searching for opportunities.
