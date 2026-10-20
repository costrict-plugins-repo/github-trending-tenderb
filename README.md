# TenderB — Government Contract Bid Management Plugin

An AI-powered bid management plugin for government contractors. Covers the full bid lifecycle from opportunity discovery through post-award analysis — designed for teams pursuing federal, state, and local government contracts in the United States.

## Installation

Install from the Claude marketplace, or manually:

```bash
/plugin install https://github.com/tenderb/tenderb_claude
```

## Live Data (MCP Server)

The plugin connects to the **TenderB GovCon Scout MCP server** for real-time access to 13 US government databases: SAM.gov, USASpending, Grants.gov, FPDS, Federal Register, USAJobs, Regulations.gov, GovInfo, and more.

- **Free**: 20 searches/month — connect and authenticate at [mcp.tenderb.us](https://mcp.tenderb.us)
- **Pro** ($49/mo): Unlimited searches
- **Team** ($149/mo): 5 seats, unlimited searches

Sign up at [mcp.tenderb.us/signup](https://mcp.tenderb.us/signup). The plugin's `.mcp.json` is pre-configured — just authenticate when prompted.

Without the MCP server, the plugin still works using Claude's built-in web search for opportunity discovery.

## Who It's For

- **Bid Managers** — End-to-end proposal coordination
- **Capture Managers** — Pre-RFP positioning and competitive intelligence
- **Proposal Writers** — Technical, management, and cost volume development
- **Business Development** — Pipeline building and opportunity qualification
- **Small businesses** entering government contracting for the first time

## What It Does

| Phase | Capabilities |
|-------|-------------|
| **Find** | Search SAM.gov, set up monitoring scouts, map NAICS/PSC codes |
| **Qualify** | 7-factor bid/no-bid scoring, capacity checks, strategic assessment |
| **Capture** | Win strategy, competitive analysis, customer research, ghost themes |
| **Analyze** | Extract Section L/M/C requirements, build compliance matrices, flag risks |
| **Plan** | Volume structure, color team schedule, section assignments, effort estimates |
| **Write** | Technical approach, management, past performance, cost narratives — optimized for evaluation criteria |
| **Price** | Cost models, rate buildups, BOE, price-to-win analysis |
| **Review** | Pink/Red/Gold/White Glove team reviews with evaluator-style scoring |
| **Submit** | Document assembly, format verification, portal prep, orals preparation |
| **Learn** | Win/loss debriefs, lessons learned, KPI tracking, continuous improvement |

Plus supporting capabilities:
- **Procurement Law** — FAR/DFARS guidance, set-asides, protests, compliance
- **Company Profile** — SAM registration, capability statements, certifications
- **Pipeline Management** — Dashboard, capacity planning, deadline tracking
- **Contract Analysis** — Review government T&Cs against your own terms
- **Reference Writing** — Past performance narratives, CPARS-aligned descriptions
- **Checklist Filling** — Compliance matrices, requirement trackers in spreadsheet format

## Getting Started

### Quick Start
```
/tenderb:setup     → Set up your company profile
/tenderb:search    → Find matching opportunities
/tenderb:dashboard → View your pipeline
```

### Slash Commands

| Command | What It Does |
|---------|-------------|
| `/tenderb:setup` | Initialize or update your company profile |
| `/tenderb:search` | Find government contract opportunities |
| `/tenderb:score` | Run bid/no-bid qualification on an opportunity |
| `/tenderb:analyze` | Analyze solicitation documents (upload PDFs) |
| `/tenderb:plan` | Create a proposal response plan with timeline |
| `/tenderb:write` | Write a specific proposal section |
| `/tenderb:review` | Red Team review of proposal drafts |
| `/tenderb:dashboard` | Pipeline overview with metrics |

### Skills (Auto-Triggered)

Skills activate automatically when relevant. You don't need to invoke them — just describe what you need and the right skill fires.

## Data Storage

All data is stored locally on your machine:

```
~/TenderB/
├── profile.json              # Your company capabilities
├── history.json              # Win/loss record
├── projects/
│   └── {project-name}/
│       ├── project.json      # Metadata, status, deadline
│       ├── analysis.md       # Solicitation analysis
│       ├── capture-plan.md   # Win strategy
│       ├── bid-plan.md       # Response plan & schedule
│       ├── sections/         # Written proposal sections
│       └── pricing/          # Cost models & narratives
├── scouts/                   # Saved search configurations
└── templates/                # Reusable content library
    ├── boilerplate/          # Company overview, certs
    ├── technical-approach/   # Technical templates
    ├── management-approach/  # Management templates
    ├── past-performance/     # Reference narratives
    ├── cost/                 # Rate tables, BOE templates
    └── resumes/              # Key personnel resumes
```

## Customization

- **Add your terms**: Drop your standard T&Cs into `~/TenderB/templates/boilerplate/company-terms.md` for contract analysis
- **Build your library**: Save winning proposal sections as templates for reuse
- **Connect tools**: Edit `.mcp.json` to add MCP servers for SAM.gov API, CRM, or project management tools

## Connectors

The plugin works standalone with web search for opportunity discovery. For deeper integration, configure MCP servers in `.mcp.json`:

| Connector | Purpose |
|-----------|---------|
| SAM.gov API | Direct opportunity search and document retrieval |
| GovWin/Deltek | Forecasted opportunities and intelligence |
| Microsoft 365 | Document creation and collaboration |
| Notion / Asana | Bid project tracking |

## Structure

```
tenderb/
├── .claude-plugin/plugin.json
├── .mcp.json
├── README.md
├── commands/
│   ├── search.md
│   ├── score.md
│   ├── analyze.md
│   ├── plan.md
│   ├── write.md
│   ├── review.md
│   ├── dashboard.md
│   └── setup.md
└── skills/
    ├── opportunity-discovery/SKILL.md
    ├── bid-qualification/SKILL.md
    ├── capture-planning/SKILL.md
    ├── solicitation-analysis/SKILL.md
    ├── bid-planning/SKILL.md
    ├── proposal-writing/SKILL.md
    ├── pricing-commercial/SKILL.md
    ├── quality-review/SKILL.md
    ├── submission-prep/SKILL.md
    ├── post-bid-analysis/SKILL.md
    ├── knowledge-management/SKILL.md
    ├── procurement-law/SKILL.md
    ├── company-profile/SKILL.md
    ├── pipeline-management/SKILL.md
    ├── contract-analysis/SKILL.md
    ├── reference-writing/SKILL.md
    └── checklist-filling/SKILL.md
```

## License

Apache-2.0

---

Built by [TenderB](https://tenderb.com) — Europe's first autonomous AI platform for tender and procurement management.
