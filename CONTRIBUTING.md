# Contributing to Perplexity Logging

This repository is designed for personal use but welcomes improvements to templates, scripts, and shortcuts.

## Workflow
- Work on the `dev` branch for all changes.
- Test locally before merging to `main`.
- Keep commits focused and descriptive.

## Adding New Topics
- Create a new folder under `topics/` with a lowercase, hyphenated name (e.g., `topics/new-category/`).
- Update `topics/README.md` to document the new category.

## Improving Scripts
- Ensure scripts remain cross-platform compatible (bash + fallback to Python where needed).
- Test on both Unix-like systems and Windows (Git Bash, WSL).
- Keep output minimal and informative.

## Updating Shortcuts
- Edit the corresponding `.md` file in `shortcuts/`.
- Test the updated prompt in Perplexity before committing.
- Document any new required capabilities or model settings.

## Template Changes
- Modifications to `templates/summary_template.md` should preserve existing field structure.
- Add new optional sections at the end to maintain backward compatibility.

## Pull Requests
- Not currently accepting external PRs, but feel free to fork and adapt for your own use.
