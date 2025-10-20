# Changelog

All notable changes to this project will be documented in this file.

## [1.0.0] - 2025-10-13

### Added
- Initial production release
- Manual workflow for creating conversation summaries
- `scripts/quick-summary.sh` for rapid local summary creation
- Perplexity shortcuts (`/save`, `/recent`, `/find`) with MCP integration
- Comprehensive documentation (`README.md`, `docs/workflow.md`, `CONTRIBUTING.md`)
- GitHub Actions CI pipeline for validation
- Topic-based organization system
- Summary template with frontmatter support

### Features
- Cross-platform bash script with Python fallback for date handling
- Context-aware `/recent` shortcut for relevant conversation retrieval
- Layered search strategy in `/find` shortcut
- Automatic URL and session ID extraction in `/save`
- Topic folder auto-creation
- Git-based version control and backup

### Documentation
- Quick start guide in README
- Detailed workflow patterns and best practices
- Contributing guidelines for future improvements
- Topic category reference guide

### Infrastructure
- CI validation checking file structure and naming conventions
- Script syntax validation
- Placeholder detection in summaries
