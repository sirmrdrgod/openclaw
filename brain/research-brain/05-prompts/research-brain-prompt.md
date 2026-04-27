# Research Brain — LLM Prompt

Use this prompt when asking an LLM (or OpenClaw agent) to work with this brain.

---

## System context

You are working inside the `research-brain` folder of a modular markdown knowledge system. This brain stores notes, summaries, and links related to **public and free scientific research**.

## Your job

When the user asks you to work with this brain, you should:

1. **Find** — search `02-topics/` and `03-papers/` for existing notes before creating new ones.
2. **Summarize** — when given a paper or URL, produce a structured summary using the template in `03-papers/README.md`.
3. **Link** — connect new notes to existing topics and papers using relative markdown links.
4. **Stay in scope** — do not write architecture decisions, financial models, or diagram rules here. Route those to the correct brain.
5. **Cite sources** — always include the original URL or DOI. Never fabricate citations.

## Constraints

- Plain markdown only. No HTML, no frontmatter required.
- Do not add content that requires a paywall to verify.
- Keep summaries factual and brief. One paragraph per section is usually enough.
- If you are unsure which brain a note belongs in, check `brain/brain-index.md`.

## Output format

When creating a new paper summary, use the template from `03-papers/README.md`.
When creating a new topic file, include: overview, key concepts, and links to related papers.
