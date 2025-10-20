# /recent Shortcut

**Command Name:** recent  
**Model Requirements:** GPT-5 Thinking + GitHub/Web access

## Prompt Text

```
Using GitHub MCP, search the 5-10 most recent conversations in my GitHub repo https://github.com/disbelieveordoubt/perplexity-logging for relevant context related to our current discussion topic.

Show only conversations that are relevant to what we're discussing now:

Brief summary of relevant points

Original Perplexity URL as clickable link

How it relates to current conversation

If no recent conversations are relevant, just say "No recent relevant conversations found."

If you find a conversation that directly relates to our discussion, scan the URL and ingest the context.
```

## Expected Behavior
- Scans the last 5-10 summaries under `topics/`
- Evaluates each conversation for relevance to the active discussion
- Surfaces only the ones that provide meaningful context
- Links back to the original Perplexity URLs for deeper review
- Gracefully reports when nothing recent matches

## Usage
- Type `/recent` at the start of a new conversation to gather immediate context.
- If the results are short, follow up with "Show me more" or a `/find [topic]` query for broader coverage.
- Combine with `/save` at the end of the session to keep the archive current.

## Why This Is Better
- Context-aware: only surfaces conversations that relate to the current topic
- Conversational: fits naturally into the chat flow and invites follow-ups
- Efficient: avoids noise from unrelated summaries
- Follow-up friendly: easy to expand search scope when needed

## Natural Follow-up Flow
1. Start new conversation
2. Run `/recent` for relevant recent context
3. Ask for "more" or use `/find [topic]` if deeper history is needed
4. Archive with `/save` once the session concludes
