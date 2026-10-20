---
description: "Initialize or update your company profile for government contracting — NAICS codes, certifications, set-aside eligibility, past performance, and key personnel."
---

# Set Up Company Profile

Initialize or update the company profile that powers bid scoring, opportunity matching, and proposal writing.

## Workflow

1. Check if `~/TenderB/profile.json` already exists
   - If yes: show current profile summary and ask what to update
   - If no: start the full setup wizard

2. Guide the user through each section conversationally:

### Company Basics
- Company name, legal name
- UEI number (replaced DUNS), CAGE code
- Location (address, city, state, zip)
- Number of employees, annual revenue, year founded

### SAM.gov Registration
- Active registration? Expiration date?
- If not registered, explain it's required for federal contracts

### Small Business Status
- SBA size standard for primary NAICS
- Certifications: 8(a), HUBZone, SDVOSB, WOSB, EDWOSB

### Capabilities
- Primary NAICS codes (help map from plain language descriptions)
- PSC codes
- Keywords describing core competencies
- Geographic coverage
- Facility clearance level

### Certifications & Vehicles
- ISO, CMMI, FedRAMP, SOC 2, etc.
- GSA Schedule, GWAC, agency IDIQs

### Preferences
- Target agencies, contract size range, contract types
- Set-aside types eligible for
- Maximum concurrent active bids

### Track Record
- Recent contracts (name, agency, value, period)
- Current win rate
- Key personnel (name, role, clearance, qualifications)

3. Save to `~/TenderB/profile.json`
4. Create the directory structure: `~/TenderB/{projects,scouts,templates,templates/boilerplate,templates/technical-approach,templates/management-approach,templates/past-performance,templates/cost,templates/resumes}`
5. Initialize `~/TenderB/history.json` as empty array
6. Offer to generate a capability statement
7. Offer to search for matching opportunities
