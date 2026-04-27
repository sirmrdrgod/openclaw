# Mermaid Templates

This folder contains reusable starting points for common diagram types.

## How to use a template

1. Copy the raw Mermaid code block from the relevant template file.
2. Replace placeholder labels with your actual content.
3. Follow the rules in `../01-renderer-rules.md` before finalizing.
4. Paste the result into a Mermaid code block in your target markdown file.
5. Verify it renders correctly in GitHub Markdown preview.

## Available templates

| File                        | Diagram type                         |
|-----------------------------|--------------------------------------|
| `flowchart-template.md`     | Generic process flowchart (TD or LR) |
| `sequence-template.md`      | Actor interaction sequence diagram   |
| `architecture-template.md`  | System context / container diagram   |

## Extending a template

If you make a specialized version of a template that is reusable (not one-off), save it in this folder with a descriptive name and add a row to the table above.
