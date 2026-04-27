# Architecture Brain — Index

## Purpose

Capture systems architecture knowledge: design patterns, implementation notes, infrastructure decisions, technology evaluations, and enterprise integration patterns.

## What belongs here

- Architecture Decision Records (ADRs)
- System design sketches and trade-off notes
- Enterprise integration and messaging patterns
- Infrastructure and deployment topology notes
- Technology evaluation summaries (build vs. buy, framework comparisons)
- Reference architectures and implementation guides

## What does not belong here

- Raw research paper summaries → use `research-brain`
- Financial operating model or cost governance → use `finance-brain`
- Mermaid syntax rules or diagram templates → use `mermaid-brain`
- Confidential client system details (use a private repo or vault)

## Folder map

```
architecture-brain/
  00-index.md          ← this file
  01-sources.md        ← reference books, standards, and trusted resources
  02-topics/           ← one file per pattern or concept area
  03-systems/          ← one file per system or component design
  04-diagrams/         ← architecture diagrams (Mermaid source + exports)
  05-prompts/          ← LLM prompt for using this brain
```

## Naming conventions

- Topic files: `02-topics/<pattern-slug>.md` (e.g., `event-driven-architecture.md`)
- System files: `03-systems/<system-slug>.md` (e.g., `api-gateway-design.md`)
- ADRs: `03-systems/adr-<NNN>-<slug>.md` (e.g., `adr-001-message-broker-choice.md`)
