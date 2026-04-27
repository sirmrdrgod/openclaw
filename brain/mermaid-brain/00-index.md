# Mermaid Brain — Index

## Purpose

Store everything needed to generate, validate, and export Mermaid diagrams reliably across renderers (GitHub, Obsidian, Draw.io handoff). This brain is about **how to draw**, not what the diagrams mean.

## What belongs here

- Renderer compatibility rules (what syntax is safe on GitHub, Obsidian, etc.)
- Reusable diagram templates (flowchart, sequence, architecture)
- Style guide for consistent, readable diagrams
- Example diagrams that demonstrate correct patterns
- Prompts that tell an LLM how to generate valid Mermaid

## What does not belong here

- Domain knowledge (research findings, architecture decisions, finance processes) → use the relevant domain brain
- Draw.io source files → store those in the relevant domain brain's `04-diagrams/` folder
- Custom CSS or renderer-specific init blocks (these are explicitly forbidden)

## Folder map

```
mermaid-brain/
  00-index.md                    ← this file
  01-renderer-rules.md           ← what is safe across renderers
  02-templates/
    README.md                    ← how to use templates
    flowchart-template.md        ← generic flowchart
    sequence-template.md         ← sequence diagram
    architecture-template.md     ← system/architecture diagram
  03-examples/
    README.md                    ← index of examples
    sample-research-to-diagram-flow.md ← end-to-end example
  04-style-guide.md              ← naming, layout, and label rules
  05-prompts/
    mermaid-generator-prompt.md  ← LLM prompt for diagram generation
```

## Core rules (summary)

1. No `%%{init: ...}%%` blocks.
2. No custom CSS classes or `classDef` with color hex values that break on dark themes.
3. No `direction` keyword inside subgraphs on older renderers — put it at the top.
4. Test every diagram in GitHub Markdown preview before committing.
