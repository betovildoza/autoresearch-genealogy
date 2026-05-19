# Spec 06: Fictional Walkthrough

**Goal:** Show one complete, privacy-safe beginner session from starting tree to reviewed output.

**Depends on:** 03, 05

## Requirements

- Create `walkthroughs/first-run.md`.
- Use only `fixtures/minimal-vault/`.
- Include:
  - Starting files.
  - Which bundle/prompt is chosen and why.
  - What the AI is allowed to do.
  - Expected output.
  - Human review.
  - Final accepted changes.
  - Remaining open questions.
- Link to `fixtures/golden-runs/01-tree-expansion.md`.

## Files

- Create: `walkthroughs/first-run.md`
- Modify: `fixtures/golden-runs/01-tree-expansion.md` if needed
- Test: `scripts/validate-repo`

## Acceptance Criteria

- [ ] Walkthrough can be completed in 30 minutes.
- [ ] It visibly skips living people.
- [ ] It shows one rejected or speculative AI finding.
- [ ] It logs a negative result.
- [ ] It ends with a human-reviewed state, not just AI output.

## Test Plan

- Run `scripts/validate-repo`.
- Manually run through the walkthrough using only fixture files.
