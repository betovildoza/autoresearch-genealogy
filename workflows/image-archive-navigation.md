# Image Archive Navigation

How to work an online image-only archive: a scanned record collection that you can browse but cannot full-text search. This is the workflow behind [13 Image Archive Deep Dive](../prompts/13-image-archive-deep-dive.md).

## When to Use This

Use this workflow when the records you need are digitized as page images but not transcribed or indexed. Examples: parish church books, civil registers, scanned probate volumes, regional digitization portals, and FamilySearch image groups with no searchable index. You navigate by collection, year, and image number, not by typing a name into a search box.

For records you already hold as local files, use [OCR Pipeline](ocr-pipeline.md). For printed local history books, use the [09 Local History Extraction](../prompts/09-bygdebok-extraction.md) prompt. For indexed memorials, use [03 Find a Grave Sweep](../prompts/03-findagrave-sweep.md).

## The Loop

1. Find the right collection
2. Triage to a candidate page range with a contact sheet
3. Read candidate pages at full size
4. Confirm the entry
5. Crop the exact row into a checked evidence image
6. Cite and log

### Stage 1: Find the Collection

Start from the archive guide for the country in `archives/`. Identify the archive, the parish or jurisdiction, the record type (births, marriages, burials, census), and a year range that brackets your target event. Record the collection path and any stable identifier in `Research_Log.md` before you start clicking. Many archives expose a per-page image ID or sequence number; that ID is the address you will cite later.

### Stage 2: Triage With a Contact Sheet

A register can run to hundreds of page images. Do not open them one at a time from the start. Build a contact sheet and read the year and section headers to narrow the range.

Most viewers offer a thumbnail or grid view. When you have the page images locally, or can fetch a sample, build a montage so you can scan many pages at once:

```bash
# Make a contact sheet from a folder of page images
montage ~/Files/Genealogy/Collection/*.jpg \
  -tile 5x -geometry 240x320+4+4 -title "Collection contact sheet" \
  ~/Files/Genealogy/Collection/_contact-sheet.jpg
```

Use the contact sheet to find where the target year begins, then record the candidate image range (for example "images 80668640 through 80668660").

### Stage 3: Read at Full Size

Open each candidate page at full resolution. Thumbnails are for triage only; never transcribe from one. Scan for the name, its patronymic or farm-name variants, and the event year. Read the handwriting directly for historic scripts.

If a scan is faint, skewed, or stained, preprocess before reading:

```bash
# Boost contrast and straighten a faint page scan
convert page.jpg -colorspace Gray -normalize -deskew 40% -sharpen 0x1 page-clean.jpg
```

### Stage 4: Confirm the Entry

When you find a candidate entry, confirm it matches on name, date, and place, and that stated parents, spouse, or witnesses are consistent with the tree. Ask whether another same-name person could explain the record. Assign an evidence tier per `reference/confidence-tiers.md`.

### Stage 5: Crop the Exact Row

The deliverable is a tight, checked crop of the one entry, not a full-page screenshot. The crop must include the full entry, including the parent or witness line, because that line is often what proves the relationship.

```bash
# Crop a single register row from a full-size page.
# Geometry is WIDTHxHEIGHT+XOFFSET+YOFFSET in pixels; read the values off the open image.
convert page-full.jpg -crop 5200x1050+620+2100 +repage \
  ~/Vaults/MyVault/Genealogy/Evidence/parish-surname-baptism-1871-80668647.jpg
```

Then inspect the crop. The single most common mistake is a crop that clips the parent line or the entry number. If the crop is low, high, or misaligned, adjust the offsets and redo it before saving. Never save a crop you have not looked at.

Store crops in an `Evidence/` folder inside your vault. If your vault is markdown-only and binaries live elsewhere, keep the crops in a parallel folder and record the absolute path in the transcription note's `evidence_crop` field.

### Stage 6: Cite and Log

Create or update a transcription note from `vault-template/templates/transcription.md`. Fill `source` and `evidence_crop`, transcribe the entry, mark unreadable text `[unclear]`, and extract facts with confidence levels.

A complete image citation names all of:

- Archive and collection (for example "Gislev parish church book, baptisms")
- Page or image ID (for example "image 80668647")
- Entry number on the page (for example "entry 18, 1871")
- The saved crop path

In `Research_Log.md`, log the collection, the image range checked, the entry found or the negative result, and the crop path. Log negative ranges explicitly so the next pass does not re-read them.

## Discipline

- **Index then image.** An index or transcription is a finding aid, never the citation. Open the linked image and confirm.
- **Page you read, not the page next door.** Cite the exact page the entry sits on.
- **Unreadable stays unreadable.** If you cannot read it, save the crop and mark facts `[unclear]`. Route it to a human rather than inventing a reading.
- **Living people are out of scope.** Do not browse, crop, or save record images for living or possibly living people during an autonomous run.
- **Respect the archive.** Honor terms of use and rate limits. Slow down rather than hammering a viewer.

## Tips

- **Cite image IDs.** A stable image ID makes a record re-findable and lets you scan a range systematically.
- **Read spine and margin dates.** Register pages carry the year and month in a header or margin; use these to jump.
- **Name the crop after the citation.** A filename like `parish-surname-event-year-imageid.jpg` ties the image to its citation at a glance.
- **Batch the contact sheets.** Build one contact sheet per collection up front, then work the candidate ranges.
