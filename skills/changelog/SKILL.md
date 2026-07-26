---
name: changelog
description: Add a user-facing entry to CHANGELOG.md for work that just landed. Use when wrapping up a feature/fix, or when asked to record what changed
---

# Changelog

Record what shipped as it lands. Do not scrape commits at release time, write the entry now while the change is fresh.

1. Open root `CHANGELOG.md`.
2. Add one bullet under `## [Unreleased]`, in the right subhead:
   - `### Added` — new features the user can see/use.
   - `### Changed` — behavior changes to existing features.
   - `### Fixed` — bug fixes.
3. Write it for a user reading release notes, not as a commit message:
   - One line, present tense.
   - Describe the effect, not the implementation or file paths.
   - Skip internal-only churn (refactors, deps, CI, tests) unless it changes
     what the user experiences.
4. Link the issue if there are any `[issue #NN](url)`

Create a subhead only if it has at least one entry.

Entries stay under `Unreleased` until `/release` promotes them to a version heading. See `.agents/skills/release`.
