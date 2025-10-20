# /save Shortcut

**Command Name:** save  
**Model Requirements:** GPT-5 Thinking + GitHub/Web access

## Prompt Text

```
Create a summary of this conversation and save it to my GitHub repo https://github.com/disbelieveordoubt/perplexity-logging via MCP as a markdown file for later reference by Perplexity:

You must:
1. Detect the exact conversation URL and session ID from the current Perplexity session. Do not leave placeholders.
2. Choose the appropriate topics/[category]/ folder.
3. Generate the filename `YYYY-MM-DD-short-title.md`.
4. Fill every field in templates/summary_template.md, including the `url:` and `sessionId:` frontmatter fields.
5. If the URL or session ID cannot be detected, stop and report the failure instead of writing an incomplete file.

After writing the file, verify the frontmatter contains url: and sessionId: with real values before committing.
```

## Expected Behavior
- Detects conversation URL automatically
- Analyzes conversation for topics and key decisions
- Chooses appropriate category from topics/ folders
- Creates properly formatted markdown file
- Commits to repository

## Usage
Type `/save` at end of any Perplexity conversation to archive it.
