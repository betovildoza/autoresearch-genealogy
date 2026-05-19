# First Run Walkthrough

This walkthrough shows one complete beginner session using only fictional data.

You can finish it in about 30 minutes. Do not use real family data for this walkthrough.

## Starting Files

Open these files:

- [fixtures/minimal-vault/Family_Tree.md](../fixtures/minimal-vault/Family_Tree.md)
- [fixtures/minimal-vault/Open_Questions.md](../fixtures/minimal-vault/Open_Questions.md)
- [fixtures/minimal-vault/Research_Log.md](../fixtures/minimal-vault/Research_Log.md)
- [fixtures/golden-runs/01-tree-expansion.md](../fixtures/golden-runs/01-tree-expansion.md)

The fixture contains:

- 2 living people: Jordan Example and Alex Example.
- 3 deceased ancestors: Eleanor Reed, Samuel Reed, and Clara Whitfield.
- 1 source conflict: Samuel Reed's birth year.
- 2 open questions.

## Choose The Workflow

Use [Prompt Picker](../guides/prompt-picker.md).

This fixture has:

- A genealogy folder.
- Living people clearly marked.
- Some source notes.
- A known contradiction.

The next action is [02 Cross-Reference Audit](../prompts/02-cross-reference-audit.md) if you are actually working the tree.

For this walkthrough, read [01 Tree Expansion](../prompts/01-tree-expansion.md) and the matching [Golden Run](../fixtures/golden-runs/01-tree-expansion.md) so you can see how expansion is supposed to behave safely.

## What The AI Is Allowed To Do

Allowed:

- Search only deceased people in the fixture.
- Add speculative leads when a source is weak.
- Log negative results.
- Leave unresolved conflicts unresolved.

Not allowed:

- Search Jordan Example or Alex Example.
- Add exact private details for living people.
- Treat fixture records as real records.
- Add confirmed ancestors without evidence.

## Expected Output

The golden run expects:

- Living people skipped: Jordan Example and Alex Example.
- New confirmed individuals added: 0.
- New speculative leads added: 2.
- Conflicts resolved: 0.
- Negative searches logged: 1.

The important part is not the count. The important part is the behavior: safety first, sources before facts, and uncertainty preserved.

## Human Review

Open [Review Card: Tree Expansion](../review-cards/01-tree-expansion.md).

Check:

- Did the run skip living people?
- Did each proposed lead include a source or reason?
- Did speculative leads stay speculative?
- Did the run log a failed search for Clara Whitfield?
- Did the run avoid “fixing” the Samuel Reed 1904 vs 1905 conflict without stronger evidence?

## Final Accepted Changes

For this fictional walkthrough, accept only:

- A speculative lead that Samuel Reed's possible parents may be Martin Reed and Helen Carter, because the golden run labels it synthetic and unverified.
- A negative-result log entry for Clara Whitfield.

Do not accept:

- Any confirmed new ancestor.
- Any living-person search.
- Any birth-year resolution for Samuel Reed.

## Remaining Open Questions

Keep these open:

- Who were Samuel Reed's parents?
- Was Samuel Reed born in 1904 or 1905?

## What Wrong Looks Like

Reject the run if:

- It searches living people.
- It confirms Martin Reed or Helen Carter as parents.
- It invents parents for Clara Whitfield.
- It removes the Samuel Reed birth-year conflict.
- It does not log failed searches.

## Next Real Workflow

When you move from the fixture to your own data:

1. Use `guides/privacy-mode.md`.
2. Use [First Week Checklist](../checklists/first-week-checklist.md).
3. Use [Prompt Picker](../guides/prompt-picker.md).
4. Read the review card before accepting any AI changes.

