# Perplexity Shortcuts

This folder contains the shortcut definitions used in Perplexity conversations.

## Available Shortcuts
- `/save` – Archive the active conversation (`shortcuts/save.md`).
- `/archive [URL]` – Archive a past conversation via URL (`shortcuts/archive.md`).
- `/recent` – Review the latest relevant summaries with heuristics (`shortcuts/recent.md`).
- `/find [topic]` – Search the full archive (`shortcuts/find.md`).
- `/resume [hint]` – Surface today/yesterday summaries to continue workstreams (`shortcuts/resume.md`).

## Setup Instructions
1. In Perplexity, open Settings → Complexity
2. Create new shortcut
3. Copy prompt text from the corresponding `.md` file
4. Set model requirements as specified
5. Save and test

## Iteration Process
- Edit shortcut `.md` files to improve prompts
- Test changes in Perplexity
- Commit improvements to the repository
- Version control allows rollback if needed
- Combine `/resume`, `/recent`, `/find`, and `/save` for resume → context → deep search → archive
- Refer to `README.md` for the overall workflow summary

## Future Shortcuts
Add new shortcut definitions here as needed.
