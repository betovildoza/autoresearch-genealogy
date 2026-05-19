# Spec 03: Prompt Bundles

**Goal:** Package prompts into copy-paste workflows so beginners do not have to choose from 12 prompt files.

**Depends on:** 02

## Requirements

- Create `guides/bundles/`.
- Add these bundles:
  - `beginner-pack.md`
  - `document-pack.md`
  - `dna-pack.md`
  - `verification-pack.md`
  - `advanced-pack.md`
- Each bundle includes:
  - Who it is for.
  - What to prepare.
  - Prompt order.
  - Stop conditions.
  - Human review checklist links.
  - Expected outputs.
- Bundles link to existing prompts, not duplicate the full prompt text.

## Files

- Create: `guides/bundles/beginner-pack.md`
- Create: `guides/bundles/document-pack.md`
- Create: `guides/bundles/dna-pack.md`
- Create: `guides/bundles/verification-pack.md`
- Create: `guides/bundles/advanced-pack.md`
- Modify: `README.md`
- Test: `scripts/validate-repo`

## Acceptance Criteria

- [ ] Beginner Pack starts with setup, privacy, and source inventory before tree expansion.
- [ ] Verification Pack includes cross-reference and source citation audit.
- [ ] DNA Pack warns against assigning ethnicity to a specific ancestor without documentary evidence.
- [ ] Every bundle has a clear “stop and review” point.

## Test Plan

- Run `scripts/validate-repo`.
- Check all prompt links.
