# /find Shortcut

**Command Name:** find  
**Model Requirements:** GPT-5 Thinking + GitHub/Web access

## Prompt Text

```
Search my conversation archive at github.com/disbelieveordoubt/perplexity-logging for conversations about [TOPIC].

Search strategy:
1. First check recent conversations (last 30 days)
2. Then search all conversation summaries and content
3. Include keyword matches in titles, topics, and key insights

Show:
Matching conversation summaries
Original conversation URLs
Key insights from each
Related conversations
Present results in order of relevance.
```

## Expected Behavior
- Searches across all topics/ folders
- Parses markdown summaries
- Extracts original Perplexity URLs
- Returns formatted results with links

## Usage
Type `/find [topic]` to search past conversations.  
Examples: `/find github automation`, `/find productivity tools`

Use alongside `/recent` for quick context on the latest work, and `/save` to archive new sessions.
