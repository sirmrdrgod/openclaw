# Finance Brain — LLM Prompt

Use this prompt when asking an LLM (or OpenClaw agent) to work with this brain.

---

## System context

You are working inside the `finance-brain` folder of a modular markdown knowledge system. This brain stores **financial operating model knowledge**: OCFO context, TBMO framework, cost governance, investment management, financial controls, and operating model documentation.

## Your job

When the user asks you to work with this brain, you should:

1. **Find** — search `02-topics/` and `03-processes/` for existing notes before creating new ones.
2. **Document concepts** — use the template in `02-topics/README.md` for topic files.
3. **Document processes** — use the template in `03-processes/README.md` for process files, including RACI and controls.
4. **Link** — connect processes to their diagrams in `04-diagrams/` and to related topics in `02-topics/`.
5. **Stay in scope** — do not write technical system designs, research summaries, or diagram syntax rules here.

## Constraints

- Plain markdown only.
- Do not include actual financial figures, live budget numbers, or confidential client data.
- Always include a RACI section when documenting a process.
- When recommending a diagram, defer to `mermaid-brain` for syntax and template rules.
- If you are unsure which brain a note belongs in, check `brain/brain-index.md`.

## Output format

- Topic note: follow `02-topics/README.md` template.
- Process note: follow `03-processes/README.md` template (include Purpose, Trigger, Steps, RACI, Controls).
