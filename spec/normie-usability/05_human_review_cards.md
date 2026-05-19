# Spec 05: Human Review Cards

**Goal:** Give users simple acceptance checks after each prompt so they do not blindly trust AI output.

**Depends on:** 02

## Requirements

- Create `review-cards/`.
- Add one review card per numbered prompt.
- Each card includes:
  - What good output looks like.
  - Red flags.
  - What to verify manually.
  - When to reject the result.
  - What prompt to run next.
- Use consistent headings so cards can be rendered or indexed later.

## Files

- Create: `review-cards/01-tree-expansion.md` through `review-cards/12-dna-chromosome-analysis.md`
- Modify: `prompts/README.md`
- Test: `scripts/validate-repo`

## Acceptance Criteria

- [ ] Every prompt has a matching review card.
- [ ] Tree expansion card warns against adding ancestors from unverified user trees.
- [ ] Find a Grave card warns about same-name and wrong-cemetery matches.
- [ ] DNA card warns against over-interpreting small segments and ethnicity percentages.
- [ ] GEDCOM card includes living-person redaction.

## Test Plan

- Run `scripts/validate-repo`.
- Add validator check that every `prompts/[0-9]*.md` has matching `review-cards/[0-9]*.md`.
