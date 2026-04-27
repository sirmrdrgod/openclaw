# Brain System

This folder contains a set of modular, markdown-based "brains" that can be read by OpenClaw agents, edited in Obsidian, and versioned in GitHub.

## How it works

Each brain is a self-contained folder of plain markdown files organized around a specific domain of knowledge. There are no databases, APIs, or background processes — just text files.

```
brain/
  brain-index.md        ← start here to pick the right brain
  README.md             ← this file

  research-brain/       ← public research, paper summaries, free sources
  architecture-brain/   ← systems design, patterns, implementation notes
  finance-brain/        ← cost governance, operating model, controls
  mermaid-brain/        ← diagram generation, templates, renderer rules
```

## Design principles

- **Plain markdown only.** No proprietary formats, no frontmatter required.
- **Obsidian-friendly.** Every folder has a README or index so navigation works in any editor.
- **GitHub-safe.** All Mermaid diagrams use renderer-safe syntax.
- **Agent-readable.** Each brain has a `05-prompts/` file that tells an LLM how to use it.
- **No lock-in.** Copy any folder out and it still makes sense on its own.

## Adding content

1. Find the right brain using `brain-index.md`.
2. Open the brain's `00-index.md` to confirm it belongs there.
3. Drop your note in the relevant numbered subfolder.
4. Link it from the brain's `00-index.md` if it is a key document.

## Extending

To add a new brain, create a new folder following the same numbered-subfolder pattern and add an entry to `brain-index.md`.
