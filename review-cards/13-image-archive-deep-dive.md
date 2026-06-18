# Review Card: Image Archive Deep Dive

Prompt: [13 Image Archive Deep Dive](../prompts/13-image-archive-deep-dive.md)

## Good Output

- Every confirmed event names the archive, collection, page or image ID, and entry number.
- Every confirmed event has a saved crop in the evidence folder, and the crop shows the full entry including the parent or witness line.
- The transcription marks unreadable text as `[unclear]` instead of guessing.
- Page ranges that were checked with no match are logged as negative results.
- Index or transcription hints are treated as finding aids, with the original image confirmed separately.

## Red Flags

- A confident transcription of a faint or illegible scan with no `[unclear]` marks.
- A citation that names the collection but not the page or image, so the record cannot be re-found.
- A crop that clips the parent, spouse, or witness line, or a full-page screenshot standing in for a row crop.
- An event recorded from an index entry without opening the linked image.
- A burial, birth, or marriage attributed to a neighboring page rather than the page actually read.
- Any crop or search touching a living or possibly living person.

## Verify Manually

- Open the cited image at full size and confirm the entry says what the transcription claims.
- Check that the saved crop matches the cited entry and is not a different same-name row.
- Confirm the name, date, and place align, and that stated relatives are consistent with the tree.
- Re-read any line marked `[unclear]` yourself before trusting an extracted fact built on it.

## Reject The Result When

- The crop or citation does not let you re-find the exact entry.
- The entry was read from an index rather than the original register.
- The dates or place conflict with known facts and the conflict was not routed to `Open_Questions.md`.
- The transcription fills illegible text with a confident guess.

## Next Prompt

Run [02 Cross-Reference Audit](../prompts/02-cross-reference-audit.md) to reconcile the new image-backed facts against the rest of the tree, then [05 Source Citation Audit](../prompts/05-source-citation-audit.md).
