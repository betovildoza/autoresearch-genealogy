# Spec 08: Obsidian-Lite Setup

**Goal:** Make the toolkit usable for people who do not want to learn Obsidian.

**Depends on:** 01

## Requirements

- Create `guides/no-obsidian-setup.md`.
- Explain folder usage with Finder, Explorer, or any markdown editor.
- Show minimal file set:
  - `Family_Tree.md`
  - `Research_Log.md`
  - `Open_Questions.md`
  - `Data_Inventory.md`
- Explain wikilinks in plain language.
- Include “just use search in your folder” fallback.

## Files

- Create: `guides/no-obsidian-setup.md`
- Modify: `workflows/getting-started.md`
- Modify: `README.md`
- Test: `scripts/validate-repo`

## Acceptance Criteria

- [ ] User can start without installing Obsidian.
- [ ] Guide works on Mac and Windows conceptually.
- [ ] No command-line requirement.
- [ ] Links from Start Here and README.

## Test Plan

- Run `scripts/validate-repo`.
- Manually review for jargon.
