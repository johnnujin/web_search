---
name: web-search
description: Search the live web for current information using Google Search.
---

# Web Search

## Instructions

Call the `run_js` tool using `index.html` and pass the search query as a plain string in `data` (not JSON).

**When to invoke:**
- Current events, news, sports scores, weather, anything recent
- Any question you are not confident answering from memory

**Reading results:**
The tool returns a JSON object like this:
```json
{
  "query": "nba finals 2026 winner",
  "results": [
    {
      "title": "2026 NBA Finals",
      "link": "https://en.wikipedia.org/...",
      "snippet": "The New York Knicks defeated the San Antonio Spurs..."
    }
  ]
}
```
Read the `snippet` fields and synthesize a direct answer. Always answer based on what the snippets say — do not say you could not find results if the results array is non-empty.
