# Finance Brain — Index

## Purpose

Capture financial operating model knowledge: OCFO context, TBMO (Target Business and Management Operating Model), cost governance, investment management, financial controls, and operating model documentation.

## What belongs here

- OCFO scope, mandate, and operating principles
- TBMO framework notes and implementation guidance
- Cost governance policies, thresholds, and approval flows
- Investment management processes and portfolio tracking notes
- Financial controls documentation (segregation of duties, reconciliation, audit trail)
- Operating model descriptions, RACI matrices, and decision rights

## What does not belong here

- Technical system designs → use `architecture-brain`
- Public research paper summaries → use `research-brain`
- Diagram syntax or templates → use `mermaid-brain`
- Actual financial data, live numbers, or confidential client information (use a private vault)

## Folder map

```
finance-brain/
  00-index.md          ← this file
  01-sources.md        ← frameworks, standards, and reference material
  02-topics/           ← one file per concept or domain area
  03-processes/        ← one file per process or workflow
  04-diagrams/         ← process maps, RACI charts, operating model diagrams
  05-prompts/          ← LLM prompt for using this brain
```

## Naming conventions

- Topic files: `02-topics/<slug>.md` (e.g., `cost-governance.md`, `tbmo-overview.md`)
- Process files: `03-processes/<slug>.md` (e.g., `budget-approval-flow.md`)
