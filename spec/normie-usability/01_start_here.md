# Spec 01: Start Here

**Goal:** Create a one-page first stop that tells nontechnical users exactly where to begin.

**Depends on:** none

## Requirements

- Create `START_HERE.md`.
- Use plain language, no repo jargon in the first screen.
- Route users by situation:
  - I only have names and family stories.
  - I have old documents or photos.
  - I have DNA results.
  - I already have a tree.
  - I want to verify an AI finding.
  - I want to export or share safely.
- Include a 30-minute first-run path.
- Include a privacy warning before any AI/web-search step.
- Link to setup paths for Obsidian and no-Obsidian usage.

## Files

- Create: `START_HERE.md`
- Modify: `README.md`
- Test: `scripts/validate-repo`

## Acceptance Criteria

- [ ] A nontechnical user can identify their next step from the first page.
- [ ] `README.md` points to `START_HERE.md` before Quick Start.
- [ ] The page links to prompt picker, bundles, checklists, privacy mode, and walkthrough placeholders.
- [ ] The page does not require knowing what `/autoresearch` means before choosing a path.

## Test Plan

- Run `scripts/validate-repo`.
- Manually verify every link resolves.
