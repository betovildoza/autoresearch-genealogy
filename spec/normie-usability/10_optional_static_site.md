# Spec 10: Optional Static Site

**Goal:** Scope a future docs site only after the markdown flow is proven.

**Depends on:** 01, 02, 03, 04, 05, 06, 07, 08, 09

## Requirements

- Do not implement in MVP.
- Evaluate whether a static site would reduce friction after markdown docs exist.
- Candidate stack should be boring:
  - GitHub Pages with plain Markdown, or
  - MkDocs Material, or
  - Docusaurus only if navigation needs justify it.
- Keep repo usable without the site.

## Files

- Create later: `docs-site/` or site config
- Modify later: `.github/workflows/`

## Acceptance Criteria

- [ ] Decision only after MVP docs are complete.
- [ ] Site build does not become required to use the repo.
- [ ] Navigation mirrors `START_HERE.md`, prompt picker, bundles, checklists, and walkthrough.

## Test Plan

- Future: run static site build in CI if adopted.
