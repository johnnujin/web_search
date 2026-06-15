---
name: web-search
description: Search the live web for current information (news, prices, facts after the model's training cutoff, real-time data) using the Serper.dev Google Search API.
metadata:
  require-secret: true
  require-secret-description: Get a free API key from https://serper.dev (sign up, then copy your API key from the dashboard).
  homepage: https://github.com/johnnujin/web_search
---

# Web Search

## Instructions

Call the `run_js` tool using `index.html` and a JSON string for `data` with the following field:

- **query**: Required. A short, focused search query (2-6 words) capturing the key terms needed to answer the user's question. Strip conversational language and keep only the distinctive nouns/terms.

**When to invoke this skill:**
- The user asks about current events, news, prices, scores, weather, or anything that could have changed recently.
- The user asks about a specific named entity you are not confident about or that may not exist in your training data.
- The user explicitly asks you to search the web or "look something up."

**Handling results:**
- The tool returns a JSON object with a `results` array, each containing `title`, `link`, and `snippet`.
- Read through the snippets and synthesize a concise answer in your own words. Do NOT quote snippets verbatim at length.
- If `results` is empty or an `error` field is present, tell the user the search didn't return useful results rather than guessing.

**Constraints:**
- Keep your final answer to 2-4 sentences unless the user asks for more detail.
- Always respond in the same language as the user's original prompt.
