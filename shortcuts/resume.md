# /resume Shortcut

**Command Name:** resume  
**Model Requirements:** GPT-5 Thinking + GitHub/Web access

## Prompt Text

```
Use GitHub MCP to locate the most recent conversation summaries so we can resume ongoing work without loading the entire archive.

Search constraints:
1. Limit the search to `topics/` files whose filenames match `YYYY-MM-DD-*.md` dated today or yesterday.
2. Prioritize matches whose titles or topic tags contain the supplied hint (default: current project).
3. If nothing matches within that two-day window, offer to expand the search with `/recent` or `/find` instead of doing it automatically.

For each matching summary, provide:
- A one-sentence recap (max 35 words)
- Key decisions or blockers (up to 3 bullets)
- Follow-up items flagged with `[ ]` checkboxes when possible
- The file path and original Perplexity URL

After listing the summaries, offer a next step:
- If a summary looks relevant, ask whether to ingest the full conversation via its URL.
- If none are relevant, suggest capturing a new summary with `/save` or `/archive`.

Keep the tone concise and operational. Avoid rewriting the summaries.
```

## Expected Behavior
- Scans only `topics/` entries dated today or yesterday
- Returns short recaps with decisions, blockers, and follow-ups
- Provides file path and URL for quick access
- Offers to ingest the full log only on user confirmation
- Suggests fallback commands when nothing matches

## Usage
- Type `/resume [optional hint]` at the start of a session to pick up yesterday’s work.
- Example: `/resume linkedin skills` focuses on recent files mentioning LinkedIn skills.
- If no hint is provided, the shortcut returns the most recent summaries for manual review.
