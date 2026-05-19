# Spec 04: Checklists

**Goal:** Add printable, task-oriented checklists for common beginner workflows.

**Depends on:** 01

## Requirements

- Create `checklists/`.
- Add:
  - `first-week-checklist.md`
  - `scan-your-documents.md`
  - `interview-a-relative.md`
  - `verify-an-ai-finding.md`
  - `before-you-add-an-ancestor.md`
  - `share-safely.md`
- Use checkbox format throughout.
- Keep each checklist to one screen or printable page where possible.
- Link each checklist to relevant workflows and prompts.

## Files

- Create: `checklists/*.md`
- Modify: `workflows/README.md` only if a workflows index is added later
- Test: `scripts/validate-repo`

## Acceptance Criteria

- [ ] Checklists are usable without reading methodology docs first.
- [ ] `verify-an-ai-finding.md` requires source review before accepting a new fact.
- [ ] `share-safely.md` includes living-person redaction.
- [ ] `before-you-add-an-ancestor.md` blocks single-source tree-copying.

## Test Plan

- Run `scripts/validate-repo`.
- Print-preview or manually inspect for length and scannability.
