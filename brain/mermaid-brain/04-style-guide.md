# Mermaid Style Guide

Rules for consistent, readable, and renderer-safe diagrams across all brains.

---

## Labels

- Use title case for node labels: `Process Payment`, not `process payment`.
- Keep labels short — aim for 1–4 words. Move detail into a linked markdown note.
- Quote labels that contain special characters: `A["Payment (USD)"]`.
- Use plain text only. No HTML tags, no emoji, no Unicode arrows.

## Edge labels

- Edge labels should be 1–3 words: `-->|Approves|`, not `-->|Approves the request after review|`.
- Put the label close to the source node logically.

## Node IDs

- Use short uppercase or camelCase IDs: `A`, `B`, `PaySvc`, `DB`.
- IDs are internal — they do not appear in the rendered output.
- Avoid IDs that shadow Mermaid keywords: `end`, `graph`, `subgraph`.

## Layout

- Use `flowchart TD` (top-down) for process flows and approval chains.
- Use `flowchart LR` (left-right) for pipelines and data flows.
- Group related nodes in a subgraph. Keep subgraph names to 1–3 words.
- Avoid crossing edges where possible — reorder nodes to reduce visual clutter.

## Subgraph naming

- Use PascalCase for subgraph names: `subgraph AuthService`.
- One concept per subgraph. Do not put unrelated nodes in the same subgraph.

## Diagram size

- Target 5–15 nodes for most diagrams. Split into multiple diagrams if larger.
- Context diagram: ≤10 nodes.
- Container diagram: ≤15 nodes.
- Sequence diagram: ≤6 participants, ≤12 messages.

## Shape conventions (flowchart)

| Shape       | Meaning                        |
|-------------|--------------------------------|
| `[text]`    | Process step or component      |
| `(text)`    | Soft boundary, grouping label  |
| `([text])`  | Start or end terminal          |
| `{text}`    | Decision / branch              |
| `[(text)]`  | Database or storage            |
| `[/text/]`  | Input or output                |

## Color and theme

- Do not set colors. Use the renderer's default theme.
- Never use `classDef` with hex values — they conflict with dark mode renderers.
- If you need visual grouping, use subgraphs instead of color.

## Versioning diagrams

- When a diagram changes significantly, update it in place.
- If the old version is still useful (e.g., a before/after comparison), copy it to `03-examples/` with a versioned name before editing.
