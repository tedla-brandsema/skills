# Changelog

## 3.1.0

### Added

- Draft Governor assignments for the next authorized handoff using eight templates covering planning, implementation, investigation, review, and Git delivery.
- Review a named plan or implementation candidate independently in a read-only assignment. The review records a verdict, findings, and any claims that could not be verified.

### Fixed

- Corrected the checkout path in the README's local installation instructions.

## 3.0.0 (2026-11-11)

### Changed

- Replaced the coded Governor runtime with a prompt-driven Agent Skill for Codex and Claude Code. The skill follows the [Project Governor Prompt v3](governor/docs/project-governor-prompt-v3.md) and uses the agent's available tools and the target repository's checks.

### Removed

- Retired the Governor executable, workflow engine, dashboard, observation database, and qualification framework. The previous implementation remains available on `archive/governor-coded-2026-11-11`.
