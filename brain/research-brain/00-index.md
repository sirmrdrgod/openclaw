# Research Brain — Index

## Purpose

Capture public and freely accessible scientific research. This is a reading and synthesis layer — notes, summaries, and curated links — not original writing or internal proprietary analysis.

## What belongs here

- Summaries of public research papers and preprints
- Topic overviews drawn from open-access sources
- Curated links to free datasets, tools, or libraries
- Personal notes taken while reading public material
- Tags and cross-references to topics in this brain

## What does not belong here

- Internal system design or architecture decisions → use `architecture-brain`
- Financial models or cost governance notes → use `finance-brain`
- Mermaid diagram templates or renderer rules → use `mermaid-brain`
- Confidential or proprietary research

## Folder map

```
research-brain/
  00-index.md          ← this file
  01-sources.md        ← trusted source registry (journals, preprint servers, datasets)
  02-topics/           ← one file per topic area
  03-papers/           ← one file per paper or paper cluster
  04-diagrams/         ← exported or hand-crafted diagrams related to research
  05-prompts/          ← LLM prompt for using this brain
```

## Naming conventions

- Topic files: `02-topics/<slug>.md` (e.g., `transformer-architectures.md`)
- Paper files: `03-papers/<year>-<short-title>.md` (e.g., `2023-attention-is-all-you-need.md`)
