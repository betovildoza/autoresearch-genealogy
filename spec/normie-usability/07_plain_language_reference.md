# Spec 07: Plain-Language Reference

**Goal:** Translate genealogy methodology into language beginners can apply immediately.

**Depends on:** 04, 05

## Requirements

- Create `guides/plain-language/`.
- Add:
  - `source-grades.md`
  - `evidence-vs-clues.md`
  - `why-ai-can-be-wrong.md`
  - `what-counts-as-proof.md`
- Map friendly terms to formal concepts:
  - “Trust this” → strong signal.
  - “Use carefully” → moderate signal.
  - “Lead only” → speculative.
- Include small fictional examples.

## Files

- Create: `guides/plain-language/source-grades.md`
- Create: `guides/plain-language/evidence-vs-clues.md`
- Create: `guides/plain-language/why-ai-can-be-wrong.md`
- Create: `guides/plain-language/what-counts-as-proof.md`
- Modify: `reference/confidence-tiers.md`
- Modify: `reference/source-hierarchy.md`
- Test: `scripts/validate-repo`

## Acceptance Criteria

- [ ] A beginner can decide whether a source is proof, support, or only a lead.
- [ ] Formal source hierarchy remains available for advanced users.
- [ ] Examples are fictional.
- [ ] AI hallucination and source-copying risks are explained plainly.

## Test Plan

- Run `scripts/validate-repo`.
- Check all examples against privacy denylist.
