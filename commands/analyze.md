---
description: "Analyze RFP/RFQ/IFB solicitation documents. Extract requirements from Section L/M/C, build a compliance matrix, and flag risks."
---

# Analyze Solicitation Documents

Read and analyze RFP/RFQ/IFB documents to extract requirements, evaluation criteria, compliance needs, and risks.

## Workflow

1. Read all uploaded solicitation documents (PDFs, Word docs)
2. Identify the UCF sections present (A through M) and any amendments
3. Extract Section C (SOW/PWS): scope, task areas, deliverables, performance standards, period of performance
4. Extract Section L (Proposal Instructions): volume structure, page limits, format requirements, content requirements
5. Extract Section M (Evaluation Criteria): methodology (LPTA vs Best Value), factors, subfactors, relative importance, rating scale
6. Extract special requirements: clearances, certifications, key personnel, OCI, small business goals
7. Build a compliance matrix mapping every Section L requirement to response location, status, and owner
8. Identify risks: tight page limits, apparent incumbent favoritism, ambiguous SOW, unusual clauses, clearance gaps, deadline concerns, contradictions between sections
9. Extract all key dates (Q&A deadline, submission deadline, anticipated award, PoP start)
10. Save analysis to `~/TenderB/projects/{name}/analysis.md`

## Output

End with:
- Executive summary (3-5 key findings)
- Action items (questions for CO, documents to gather, sections to write)
- Top 3 risks with mitigation strategies
- Draft clarification questions
