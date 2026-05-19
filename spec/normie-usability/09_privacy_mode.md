# Spec 09: Privacy Mode

**Goal:** Give beginners explicit rules for using public AI tools without exposing living people or sensitive documents.

**Depends on:** 01

## Requirements

- Create `guides/privacy-mode.md`.
- Include:
  - What never to paste.
  - What to redact.
  - How to anonymize a prompt.
  - How to handle living people.
  - How to share a GEDCOM safely.
  - How to use the local privacy audit script.
- Provide before/after redaction examples using fictional data.

## Files

- Create: `guides/privacy-mode.md`
- Modify: `CONTRIBUTING.md`
- Modify: `prompts/README.md`
- Test: `scripts/validate-repo`
- Test: `scripts/privacy-audit-repo`

## Acceptance Criteria

- [ ] Guide is understandable before using any AI prompt.
- [ ] Includes a living-person checklist.
- [ ] Includes a “public repo safety” section for contributors.
- [ ] Links to `scripts/privacy-audit-repo`.

## Test Plan

- Run `scripts/validate-repo`.
- Run `scripts/privacy-audit-repo` with local denylist.
