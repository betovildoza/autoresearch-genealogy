# Spec 02: Prompt Picker

**Goal:** Add a decision tree that maps user state to the next best prompt or bundle.

**Depends on:** 01

## Requirements

- Create `guides/prompt-picker.md`.
- Present one-question-at-a-time style sections.
- Recommend one next prompt or bundle per endpoint.
- Include “do not run this yet” warnings for risky states:
  - living-person-heavy tree
  - no source files
  - unresolved contradictions
  - DNA-only interpretation
- Include a compact prompt matrix for users who want to browse.

## Files

- Create: `guides/prompt-picker.md`
- Modify: `prompts/README.md`
- Test: `scripts/validate-repo`

## Acceptance Criteria

- [ ] Every numbered prompt appears in the matrix.
- [ ] Each endpoint recommends exactly one next action.
- [ ] Privacy and verification prompts are recommended before expansion when appropriate.
- [ ] A user with no tree is routed to setup, not autonomous research.

## Test Plan

- Run `scripts/validate-repo`.
- Manually follow all decision-tree branches and confirm they terminate.
