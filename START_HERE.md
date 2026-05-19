# Start Here

This kit helps you use AI for family history without turning guesses into facts.

You do not need to understand this repository before you begin. Pick the situation that sounds most like you, follow that path, and stop when the page tells you to review.

## Before You Use AI

Do this first:

- Do not paste exact birth dates, addresses, phone numbers, emails, or private documents for living people into public AI tools.
- Mark living or possibly living people as `Living` or `life_status: living`.
- Keep every AI finding in “lead” status until you check the source.
- Log searches that find nothing. Negative results prevent repeated dead ends.

For the full privacy checklist, use `guides/privacy-mode.md` when it is available.

## Pick Your Starting Point

### I Only Have Names And Family Stories

Start with:

1. `workflows/getting-started.md`
2. `checklists/first-week-checklist.md`
3. `guides/bundles/beginner-pack.md`

Do not run autonomous tree expansion yet. First write down what you already know, mark living people, and list where each claim came from.

### I Have Old Documents Or Photos

Start with:

1. `checklists/scan-your-documents.md`
2. `workflows/document-triage.md`
3. `workflows/ocr-pipeline.md`
4. `guides/bundles/document-pack.md`

Your first win is turning boxes of documents into searchable notes. Do not add new ancestors until the document source is clear.

### I Have DNA Results

Start with:

1. `reference/dna-interpretation-guardrails.md`
2. `guides/plain-language/evidence-vs-clues.md`
3. `guides/bundles/dna-pack.md`

DNA can point you toward a branch. It usually cannot prove a specific ancestor by itself.

### I Already Have A Family Tree

Start with:

1. `guides/prompt-picker.md`
2. `guides/bundles/verification-pack.md`
3. `prompts/02-cross-reference-audit.md`
4. `prompts/05-source-citation-audit.md`

Verify before you expand. A bigger wrong tree is harder to fix than a smaller uncertain one.

### I Want To Check An AI Finding

Start with:

1. `checklists/verify-an-ai-finding.md`
2. `checklists/before-you-add-an-ancestor.md`
3. `review-cards/01-tree-expansion.md`

Only accept the finding if the source, identity match, dates, location, and relationship all make sense.

### I Want To Share Or Export

Start with:

1. `guides/privacy-mode.md`
2. `checklists/share-safely.md`
3. `prompts/04-gedcom-completeness.md`

Redact living people before sharing anything outside your private workspace.

## 30-Minute First Run

Use this when you want to see the loop quickly without risking real family data.

1. Open `fixtures/minimal-vault/Family_Tree.md`.
2. Open `fixtures/golden-runs/01-tree-expansion.md`.
3. Read the “Expected Safety Behavior” section.
4. Compare it with `prompts/01-tree-expansion.md`.
5. Notice that living people are skipped, speculative leads stay speculative, and negative results are logged.

That is the standard you should expect before running prompts on real research.

## The Basic Loop

Every workflow follows the same pattern:

1. Prepare the private facts you already know.
2. Choose one prompt or bundle.
3. Run it against your vault.
4. Review the sources.
5. Accept only well-supported facts.
6. Log what changed and what remains unresolved.

## If You Are Overwhelmed

Use this shortest path:

1. Copy `vault-template/` into a folder named `Genealogy`.
2. Fill in `Family_Tree.md` with only deceased ancestors at first.
3. Add living people as `Living`, without exact dates.
4. Run the verification pack before the expansion pack.
5. Stop after each prompt and review.

The goal is not to build the biggest tree. The goal is to build a tree you can trust.

If you do not use Obsidian, use [No-Obsidian Setup](guides/no-obsidian-setup.md).
