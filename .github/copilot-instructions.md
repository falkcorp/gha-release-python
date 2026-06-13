<!-- file: .github/copilot-instructions.md -->
<!-- version: 2.4.0 -->
<!-- guid: 4d5e6f7a-8b9c-0d1e-2f3a-4b5c6d7e8f9a -->
<!-- last-edited: 2026-06-13 -->

# gha-release-python — Additional Context

Org-wide coding standards (file headers, language rules, commit format) are at
**https://github.com/falkcorp/.github** and apply automatically to this repo.

For full project context: **CLAUDE.md** at the repo root.

## Project overview

GHA composite action: Python package release builds (Shell/YAML). The action
builds and publishes Python packages as part of a GitHub Actions release
workflow.

## Critical constraints

- This is a composite action — all logic lives in `action.yml` and shell steps.
- Keep changes backward-compatible; callers pin to this action by tag/SHA.
- SHA-pin all referenced GitHub Actions (no floating tags).
