# pplx-logging

> **A lightweight system for archiving and retrieving Perplexity AI conversations**

This repository stores structured summaries of Perplexity conversations so future sessions can reference prior work quickly. The workflow is lightweight, idempotent, and friendly to both manual edits and MCP-driven automation.

**Version:** 1.0.0  
**Status:** Production-ready  
**Last Updated:** 2025-10-13

## Manual Workflow
- **Copy the template**: Duplicate `templates/summary_template.md` into the appropriate folder under `topics/` (see [Topic Categories](topics/README.md)).
- **Rename**: Use the format `YYYY-MM-DD-short-title.md`.
- **Fill metadata**: Provide date, time, URL, session ID, summary, insights, decisions, and follow-ups. Link related conversations when helpful.

The script prompts for a title and topic (defaults to `general`), slugifies inputs, creates the topic folder if missing, and copies the base template into `topics/<topic>/<date>-<slug>.md` for you to fill in.

## Perplexity Shortcuts
Shortcut prompts live in `shortcuts/` and are version controlled:

- `/save` → `shortcuts/save.md`: Archives the current conversation, enforcing URL/session ID extraction.
- `/archive [URL]` → `shortcuts/archive.md`: Archives a conversation from a URL. Use this in a clean session to avoid MCP conflicts after using `/recent` or `/find`.
- `/recent` → `shortcuts/recent.md`: Pulls the most relevant recent conversations for active context.
- `/find` → `shortcuts/find.md`: Searches the full archive with a layered strategy (recent-first, then deep search).
- `/resume [hint]` → `shortcuts/resume.md`: Surfaces summaries from today or yesterday to continue active workstreams without loading every log.

Install each shortcut in Perplexity (Settings → Complexity) by copying the prompt text and setting the required capabilities.

## Searching Past Conversations
- Use Perplexity shortcuts (`/recent`, `/find`) for conversational retrieval.
- Locally, run `git grep` or GitHub code search across `topics/`.
- Each summary contains the original Perplexity URL so you can reopen the source.

## Repository Structure
- `templates/` → Canonical summary template used by scripts and shortcuts.
- `topics/` → Conversation archives organized by category. See `topics/README.md` for guidance.
- `shortcuts/` → Prompt definitions for Perplexity automation.
- `scripts/` → Utility scripts (currently `quick-summary.sh`).
- `.github/workflows/` → CI validation pipeline. (dev)

## Next Steps
- Capture new sessions using `/save` or the quick script.
- Review `/recent` at the start of a conversation for context.
- Iterate on shortcuts and documentation as the workflow evolves.

## Documentation
- **[Workflow Guide](docs/workflow.md)**: Detailed daily usage patterns, best practices, and troubleshooting. (dev)
- **[Contributing](CONTRIBUTING.md)**: Guidelines for improving scripts, shortcuts, and templates.
- **[Topic Categories](topics/README.md)**: Reference for organizing conversations by subject.
