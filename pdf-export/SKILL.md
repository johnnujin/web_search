---
name: export-pdf
description: Export any text content as a downloadable PDF file. Use when the user asks to save, export, or download content as a PDF.
---

# Export to PDF

## Instructions

Call the `run_js` tool using `index.html` and pass a JSON string for `data` with the following fields:

- **title**: Required. A short title for the PDF document (e.g. "My Summary", "Plant Care Guide").
- **content**: Required. The full text content to export. Can include multiple paragraphs separated by newlines.

**When to invoke this skill:**
- The user says "export as PDF", "save as PDF", "download this as a PDF", or similar.
- The user asks to create a document, report, or guide they can keep.
- After generating any substantial content the user might want to save.

**Example data:**
```json
{
  "title": "My Plant Care Guide",
  "content": "Monstera Deliciosa\n\nWater every 7 days. Keep in bright indirect light.\n\nPropagation\nTake a stem cutting with at least one node..."
}
```

**After calling the skill:**
Tell the user their PDF has been generated and they can tap the download/share button to save it.
