# Mermaid Renderer Rules

Rules for writing Mermaid diagrams that render correctly on GitHub, Obsidian, and can be exported to Draw.io.

---

## Golden rules

1. **No init blocks.** Never use `%%{init: { ... }}%%`. They break on GitHub and many hosted renderers.
2. **No custom CSS.** Do not use `classDef` with hex colors, `style` overrides, or renderer-specific tricks.
3. **No HTML in labels.** Labels must be plain text or quoted strings. Angle brackets and `<br>` tags fail on some renderers.
4. **Quote labels with special characters.** If a label contains `()`, `:`, `>`, or commas, wrap it in double quotes.
5. **Keep diagrams under ~40 nodes.** Larger graphs become unreadable and slow to render.

---

## Diagram type compatibility

| Type         | GitHub | Obsidian | Draw.io import | Notes                              |
|--------------|--------|----------|----------------|------------------------------------|
| `flowchart`  | ✓      | ✓        | Partial        | Most compatible; use `flowchart TD`|
| `sequenceDiagram` | ✓ | ✓       | No             | Good for interaction flows         |
| `graph`      | ✓      | ✓        | Partial        | Older alias for flowchart          |
| `classDiagram` | ✓    | ✓        | No             | OK for data models                 |
| `erDiagram`  | ✓      | ✓        | No             | Entity-relationship                |
| `gantt`      | ✓      | Partial  | No             | Timeline only; avoid complex dates |
| `pie`        | ✓      | ✓        | No             | Simple proportions only            |
| `architecture` | ✗    | ✗        | No             | Avoid — experimental, unreliable   |
| `block`      | ✗      | ✗        | No             | Avoid — not widely supported       |

---

## Flowchart direction

Use one of these at the top of a flowchart:

```
flowchart TD   ← top to bottom (most readable for process flows)
flowchart LR   ← left to right (good for pipelines)
flowchart BT   ← bottom to top (rare)
flowchart RL   ← right to left (rare)
```

Do **not** put a direction keyword inside a subgraph on older renderers.

---

## Node shapes

| Shape         | Syntax                  | Use for                       |
|---------------|-------------------------|-------------------------------|
| Rectangle     | `A[Label]`              | Process step, component       |
| Rounded rect  | `A(Label)`              | Start/end, soft boundary      |
| Diamond       | `A{Label}`              | Decision / branch             |
| Stadium       | `A([Label])`            | Terminal / endpoint           |
| Cylinder       | `A[(Label)]`           | Database / storage            |
| Parallelogram | `A[/Label/]`            | Input / output                |

---

## Edge types

| Type          | Syntax         | Use for                      |
|---------------|----------------|------------------------------|
| Arrow         | `A --> B`      | Standard flow                |
| Labeled arrow | `A -->|text| B`| Flow with annotation         |
| Dotted arrow  | `A -.-> B`     | Async or optional flow       |
| Thick arrow   | `A ==> B`      | Critical path or emphasis    |
| No arrowhead  | `A --- B`      | Association / grouping       |

---

## Subgraphs

```
subgraph GroupName
  A --> B
end
```

- Keep subgraph names short and without spaces, or quote them.
- Do not nest subgraphs more than two levels deep.

---

## Draw.io export handoff

1. Generate the Mermaid diagram and verify it renders on GitHub.
2. Copy the Mermaid source into https://mermaid.live (or Obsidian with the Mermaid plugin).
3. Export as SVG from the live editor.
4. Import the SVG into Draw.io via **Extras → Edit Diagram** or drag-and-drop.
5. Note: Draw.io import is layout-only; colors and styles will revert to Draw.io defaults.
