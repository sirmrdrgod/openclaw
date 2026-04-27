# Brain Index

Use this file to decide which brain to consult or write to.

---

## research-brain

**Use for:** public and free scientific research notes, paper summaries, topic overviews, and links to open-access sources.

**Do not use for:** internal system designs, financial models, or diagram generation rules.

Path: `brain/research-brain/`

---

## architecture-brain

**Use for:** systems architecture, design patterns, implementation notes, enterprise integration patterns, infrastructure decisions, and technology evaluations.

**Do not use for:** raw research papers, financial operating model details, or Mermaid syntax rules.

Path: `brain/architecture-brain/`

---

## finance-brain

**Use for:** OCFO context, TBMO (Target Business and Management Operating Model), cost governance, investment management, financial controls, and operating model documentation.

**Do not use for:** technical implementation details, research paper notes, or diagram templates.

Path: `brain/finance-brain/`

---

## mermaid-brain

**Use for:** Mermaid diagram generation, renderer-safe syntax rules, reusable templates (flowchart, sequence, architecture), style guides, and Draw.io export handoff notes.

**Do not use for:** domain knowledge — this brain is purely about how to draw diagrams, not what to put in them.

Path: `brain/mermaid-brain/`

---

## Quick decision table

| I want to…                                      | Use                   |
|-------------------------------------------------|-----------------------|
| Summarize a research paper                      | research-brain        |
| Note a design pattern or ADR                    | architecture-brain    |
| Document a cost governance process              | finance-brain         |
| Generate a Mermaid diagram from existing notes  | mermaid-brain         |
| Trace a flow from research → diagram            | research + mermaid    |
| Design a system end-to-end                      | architecture + mermaid|
