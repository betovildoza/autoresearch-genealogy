# UAT: Normie Usability Layer

## User Scenario 1: Names And Stories Only

- [ ] Open `START_HERE.md`.
- [ ] Choose “I only have names and family stories.”
- [ ] User is routed to setup, privacy mode, first-week checklist, and beginner pack.
- [ ] User is not routed directly into autonomous tree expansion.

## User Scenario 2: Old Documents

- [ ] Open `START_HERE.md`.
- [ ] Choose “I have old documents or photos.”
- [ ] User is routed to document checklist, OCR workflow, document bundle, and review cards.
- [ ] User sees source-quality warnings before adding facts to the tree.

## User Scenario 3: DNA Results

- [ ] Open `START_HERE.md`.
- [ ] Choose “I have DNA results.”
- [ ] User is routed to DNA guardrails, DNA bundle, and plain-language source guidance.
- [ ] User sees a warning not to assign DNA ethnicity to a specific ancestor without documentary evidence.

## User Scenario 4: Already Has A Tree

- [ ] Open prompt picker.
- [ ] User with an existing tree is routed to cross-reference audit before expansion.
- [ ] User receives review-card checks before accepting changes.

## User Scenario 5: Public Sharing

- [ ] Open privacy mode.
- [ ] User can identify what to redact before sharing a GEDCOM, prompt, or repo.
- [ ] Contributor can run `scripts/privacy-audit-repo`.

## Validation

- [ ] `scripts/validate-repo` passes.
- [ ] `scripts/privacy-audit-repo` passes with local denylist.
