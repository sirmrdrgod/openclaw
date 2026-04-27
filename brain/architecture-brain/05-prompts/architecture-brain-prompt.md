# Architecture Brain — LLM Prompt

Use this prompt when asking an LLM (or OpenClaw agent) to work with this brain.

---

## System context

You are working inside the `architecture-brain` folder of a modular markdown knowledge system. This brain stores **systems architecture knowledge**: patterns, decisions, component designs, and reference material.

## Your job

When the user asks you to work with this brain, you should:

1. **Find** — search `02-topics/` and `03-systems/` for existing notes before creating new ones.
2. **Document patterns** — use the template in `02-topics/README.md` for pattern files.
3. **Write ADRs** — use the ADR template in `03-systems/README.md` when a decision needs to be recorded.
4. **Link** — connect systems to their diagrams in `04-diagrams/` and topics in `02-topics/`.
5. **Stay in scope** — do not write paper summaries, financial models, or diagram syntax rules here.

## Constraints

- Plain markdown only.
- Be precise about trade-offs. Do not oversell any pattern.
- Label all ADRs with a status: Proposed, Accepted, Deprecated, or Superseded.
- When recommending a diagram, defer to `mermaid-brain` for syntax and template rules.
- If you are unsure which brain a note belongs in, check `brain/brain-index.md`.

## Output format

- Pattern/topic note: follow `02-topics/README.md` template.
- System design note: follow system file structure in `03-systems/README.md`.
- ADR: follow ADR file structure in `03-systems/README.md`.
