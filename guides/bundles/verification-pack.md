# Verification Pack

Use this when you already have a family tree and want to make it more trustworthy.

## Who It Is For

- You have a GEDCOM, online tree, spreadsheet, or notes from another researcher.
- You suspect some names, dates, or relationships are copied from unsourced trees.
- You want to check before expanding.

## What To Prepare

- `Family_Tree.md` populated with the current tree.
- Any source files, citations, or transcriptions you already have.
- A list of known contradictions in `Open_Questions.md`.
- Living people marked and redacted before sharing.

## Order

1. Use [Privacy Mode](../privacy-mode.md).
2. Run [02 Cross-Reference Audit](../../prompts/02-cross-reference-audit.md).
3. Run [05 Source Citation Audit](../../prompts/05-source-citation-audit.md).
4. Run [04 GEDCOM Completeness](../../prompts/04-gedcom-completeness.md) if you use GEDCOM.
5. Run [07 Timeline Gap Analysis](../../prompts/07-timeline-gap-analysis.md) after contradictions are resolved.

## Stop And Review

Stop if:

- A parent-child link comes from only one user-contributed tree.
- A person has conflicting birthplaces or spouses.
- A GEDCOM export includes living-person details.
- The AI “fixes” a conflict without explaining which source wins.

## Human Review

Use these checks before accepting changes:

- `review-cards/02-cross-reference-audit.md`
- `review-cards/05-source-citation-audit.md`
- `review-cards/04-gedcom-completeness.md`
- `review-cards/07-timeline-gap-analysis.md`
- `checklists/before-you-add-an-ancestor.md`

## Expected Outputs

- A discrepancy list.
- Under-sourced people and relationships.
- GEDCOM issues to fix.
- A clearer list of safe expansion targets.
