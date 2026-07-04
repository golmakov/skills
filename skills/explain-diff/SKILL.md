---
name: explain-diff-html
description: Use when the user asks for a rich explanation of a code change, diff, branch, or PR
---

# Explain Diff

Please make me a rich, interactive explanation of the specified code change.

## Sections

- **Background**: Explain the existing system relevant to this change. (You should broadly explore surrounding code for this). We don't know how much the reader already knows, so include a deep background for beginners (note that it can be skipped if the reader is already familiar), and then a more narrow background directly relevant to the change.
- **Intuition**: Explain the core intuition for the code change. The focus here is to explain the essence, not the full details. Use concrete examples with toy data. Use figures and diagrams liberally.
- **Code**: Do a high-level walkthrough of the changes to the code with code snippets. Group/order the changes in an understandable way. Structured more like a prose.

## Format

Output a single self-contained HTML file which includes CSS and JavaScript. Make the whole thing one long page with section headers and a table of contents. Don't use tabs for the top-level structure. Basic responsive styling so you can view it on a phone.

Put the file outside of the code repo, and start filename with today's date in `YYYY-MM-DD-` format. For example: `/tmp/2026-01-12-explanation-<slug>.html`

Write with the clarity and flow of Martin Kleppmann, making it engaging and written in classic style. Transitions between sections should be smooth. Use callouts for key concepts or definitions, important edge cases, etc.

Pick a small number of diagram families that can be reused throughout the explanation to explain various cases. Don't use ASCII diagrams.

Some useful kinds of diagrams:
  - A very simplified version of the UI that the user sees in the app, to explain UI changes.
  - A system diagram showing data flow or communication between components. Make sure to include example data here!
  - Small interactive figures
