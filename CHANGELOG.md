# Changelog

## 2026-05-19

Initial sanitized public release.

### Added
- Explicit `Inputs To Replace` sections for all numbered prompts.
- Living-person privacy guardrails for first-run genealogy workflows.
- Canonical vault file manifest and prompt path consistency rules.
- Split evidence schema: `evidence_tier` for claim quality and `profile_status` for file completeness.
- `scripts/validate-repo` plus GitHub Actions validation.
- `scripts/privacy-audit-repo` for local denylist scans across current `HEAD` and reachable Git history.
- Contribution guidance, including an optional local anonymization denylist.
- Archive guide `last_verified` metadata.
- Synthetic `fixtures/minimal-vault/` and `fixtures/golden-runs/01-tree-expansion.md` for safe prompt behavior review.
- Build scope for a markdown-first nontechnical usability layer under `spec/normie-usability/`.
- `START_HERE.md` beginner router for names, documents, DNA results, existing trees, AI findings, and sharing.
- Prompt picker, five prompt bundles, six checklists, and twelve human review cards.
- First-run walkthrough using only synthetic fixture data.
- Plain-language evidence guides for source grades, clues, AI failure modes, and proof.
- No-Obsidian setup guide for normal folders and markdown editors.
- Privacy Mode guide for redaction, GEDCOM sharing, public repo safety, and local privacy audits.

### Changed
- Public examples now use fictional names, locations, and percentages.
- GEDCOM and naming examples now use generic sample places and surnames.
- `scripts/validate-repo` now checks review-card coverage and required beginner usability files.

### Notes
- The fixture data is synthetic and should not be treated as genealogical evidence.
