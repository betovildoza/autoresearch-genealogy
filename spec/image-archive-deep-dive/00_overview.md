# Spec: Image Archive Deep Dive

## Problem

The existing prompts and the OCR pipeline assume records are either text-searchable online or already scanned to local files. A large share of genealogical truth lives in collections that are digitized but neither transcribed nor indexed: parish church books, civil registers, scanned probate volumes. You cannot search them by name. You browse page images, narrow by year and image number, read the handwriting, and confirm the entry. Nothing in the repo covered this loop, or the step of saving a cropped evidence image of the exact record row.

## Goal

Give the autoresearcher a first-class capability to exhaust an online image-only archive and produce a re-findable, image-backed citation for every event it confirms.

## Scope

- New autoresearch prompt `13-image-archive-deep-dive` following the standard prompt contract.
- Matching human review card.
- New `image-archive-navigation` workflow documenting the technique (contact-sheet triage, image-ID range scanning, full-size reading, crop-and-check, citation and logging).
- `evidence_crop` field and Evidence Image section added to the transcription template.
- Wiring: README counts and prompt table, prompts README review-card table and placeholders, prompt picker row, validate-repo prompt count, changelog.

## Non-Goals

- No automated scraping harness or archive-specific scripts. The prompt is tool-agnostic and respects each archive's terms of use and rate limits.
- No change to how indexed sources (Find a Grave, FamilySearch index) are handled; those remain finding aids confirmed against original images.

## Guardrails Preserved

- No web search, image download, or crop for living or possibly living people.
- Index entries are finding aids, not citations. The original image must be confirmed.
- Illegible text stays `[unclear]`. No confident transcription of an unreadable scan.

## Test Gate

`scripts/validate-repo` must pass, including the updated 13-prompt and 13-review-card checks, README count needles, and markdown link resolution.
