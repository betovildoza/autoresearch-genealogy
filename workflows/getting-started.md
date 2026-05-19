# Getting Started

A step-by-step guide to setting up your genealogy research vault and running your first AI-assisted research session.

## Prerequisites

- A markdown editor (Obsidian recommended, but any editor works)
- Claude Code installed (or another AI tool that supports web search and file editing)
- Whatever you already know about your family (names, dates, locations, even if incomplete)
- Any physical documents you have (photos, certificates, letters)

## Step 1: Set Up Your Vault

1. Follow [Download And Start](../guides/download-and-start.md), or clone this repository if you already use Git
2. Copy the entire `vault-template/` folder into your Obsidian vault (or your preferred location)
3. Rename it to something meaningful (e.g., `Genealogy/`)

If you do not want to use Obsidian, follow [No-Obsidian Setup](../guides/no-obsidian-setup.md). The files are plain markdown and work in Finder, File Explorer, or any text editor.

Your folder structure should look like:

```
YourVault/
└── Genealogy/
    ├── _Index.md
    ├── Family_Tree.md
    ├── Open_Questions.md
    ├── Research_Log.md
    ├── Data_Inventory.md
    ├── Timeline.md
    └── templates/
        ├── person.md
        ├── transcription.md
        └── region.md
```

## Step 2: Fill In What You Know

Open `Family_Tree.md` and start with yourself. Work backward through your parents, grandparents, and as far as you can go.

For each person, record whatever you know:
- Full name (including maiden names)
- Birth date and place (even approximate: "around 1870, somewhere in Poland")
- Death date and place
- Marriage date and spouse
- Parents' names

For living or possibly living people:
- Mark `life_status: living` or `life_status: unknown` in person files
- Use birth year only, or write `Living`
- Do not include addresses, phone numbers, emails, or exact birth dates in prompts you plan to run through web search
- Do not ask autonomous prompts to search living people

Do not worry about completeness. Gaps are what the research will fill.

**Example entry:**

```
## Paternal Line

### Smith Family

**John Smith** (b. March 15, 1935, Chicago, IL; d. January 2, 2010, Chicago, IL)
- Married Mary Jones on June 10, 1958 at St. Patrick's Church, Chicago
- Children: Robert (1960), Susan (1962), David (1965)
- Occupation: Electrician, IBEW Local 134
- Sources: family knowledge, obituary in Chicago Tribune

**Robert Smith** (b. 1905, Poland?; d. 1978, Chicago, IL)
- Father of John Smith
- Immigrated to US sometime before 1930
- Original surname may have been different
- Sources: family oral history (unverified)
```

## Step 3: Scan Your Documents

If you have physical documents (old photos, certificates, letters, postcards, military papers), scan or photograph them.

**Recommended setup:**
- Use a flatbed scanner at 300 DPI for documents, 600 DPI for photos
- If using a phone camera, use a document scanning app (not regular photos) for text documents
- Organize scans into folders by family line or document type

**File organization:**
```
~/Files/Genealogy/
├── [Family Line 1]/
│   ├── birth_certificate_john_smith.jpg
│   ├── wedding_photo_1958.jpg
│   └── military_discharge_robert_smith.jpg
└── [Family Line 2]/
    └── ...
```

Update `Data_Inventory.md` with your scan collections.

## Step 4: Choose A Safe First Prompt

Before expansion, use [Prompt Picker](../guides/prompt-picker.md).

For most first sessions, choose one of these:

- [05 Source Citation Audit](../prompts/05-source-citation-audit.md) if you need to identify weak or missing sources.
- [02 Cross-Reference Audit](../prompts/02-cross-reference-audit.md) if your tree and documents may disagree.
- [Beginner Pack](../guides/bundles/beginner-pack.md) if you want a guided order.

Do not run source-backed tree expansion until living people are protected and the starting facts are source-labeled.

## Step 5: Run A Verification Prompt

1. Open Claude Code in your genealogy vault directory, or use another AI tool that can read your files.
2. Type `/autoresearch` if your tool supports it, or paste the prompt contents directly.
3. Paste [05 Source Citation Audit](../prompts/05-source-citation-audit.md) or [02 Cross-Reference Audit](../prompts/02-cross-reference-audit.md).
2. Replace placeholders
3. Let it run

This gives you a source map and discrepancy list before the AI tries to add new ancestors.

## Step 6: Review Before Expansion

After the first verification prompt, review:

1. **Open Questions**: What gaps remain? Add them to `Open_Questions.md` with priority rankings.
2. **Person files**: For important ancestors, create person files using the template.
3. **Weak sources**: Keep unsourced relationships marked `speculative`.
4. **Next prompts**: Consider [01 Source-Backed Tree Expansion](../prompts/01-tree-expansion.md) only for deceased, source-suitable targets.

Use [Tree Expansion Review Card](../review-cards/01-tree-expansion.md) before accepting any expansion result.

## What to Do Next

- **Want to find burial records?** Run [03 Find a Grave Sweep](../prompts/03-findagrave-sweep.md)
- **Want to export your tree?** Run [04 GEDCOM Completeness](../prompts/04-gedcom-completeness.md)
- **Have scanned documents to process?** See [OCR Pipeline](ocr-pipeline.md)
- **Want to understand your DNA results?** See [DNA Interpretation Guardrails](../reference/dna-interpretation-guardrails.md)
- **Want to understand the methodology?** See [Why Autoresearch For Genealogy](../reference/why-autoresearch-for-genealogy.md)
