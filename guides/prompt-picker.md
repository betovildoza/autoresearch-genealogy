# Prompt Picker

Use this when you are not sure which prompt to run next.

Answer one section at a time. Stop when a section gives you a next action.

## First Question: Do You Have A Genealogy Folder Yet?

### No

Next action: set up the starter folder with `workflows/getting-started.md`.

Do not run an autonomous research prompt yet. A prompt needs at least `Family_Tree.md`, `Research_Log.md`, and `Open_Questions.md` so it has somewhere to put sources, searches, and unresolved claims.

### Yes

Go to the next question.

## Are Living People In The Tree?

### Yes, and they have exact dates, addresses, emails, phone numbers, or private notes

Next action: use [Privacy Mode](privacy-mode.md).

Do not run tree expansion yet. First mark living or possibly living people, remove exact private details from anything you plan to paste into a public AI tool, and decide what stays local.

### Yes, but they are marked `Living` or `life_status: living`

Go to the next question.

### No, only deceased people are in this working tree

Go to the next question.

## Do You Have Source Files Or Citations?

### No

Next action: use `checklists/first-week-checklist.md`.

Do not run tree expansion yet. First write down what you already know, where each fact came from, and which facts are family story, document-backed, or unknown.

### Yes, I have documents, citations, photos, or notes

Go to the next question.

## Are There Contradictions You Already Know About?

Examples: two birth years, two possible spouses, two people with the same name, a family story that conflicts with a record.

### Yes

Next action: run `prompts/02-cross-reference-audit.md`.

Do not expand the tree until known contradictions are visible. Expansion multiplies bad assumptions.

### No

Go to the next question.

## What Are You Trying To Do?

### I want a safe first workflow

Next action: use `guides/bundles/beginner-pack.md`.

### I want to process a box of documents or photos

Next action: use `guides/bundles/document-pack.md`.

### I want to verify an existing tree

Next action: use `guides/bundles/verification-pack.md`.

### I want to understand DNA results

Next action: use `guides/bundles/dna-pack.md`.

Do not assign ethnicity estimates or small DNA segments to a specific ancestor unless documentary records support the same relationship.

### I already have a sourced tree and want deeper searches

Next action: use `guides/bundles/advanced-pack.md`.

## Prompt Matrix

| Prompt | Use when | Review card |
|---|---|---|
| [01 Tree Expansion](../prompts/01-tree-expansion.md) | You have a sourced starter tree and want to look for parents, siblings, and older generations | `review-cards/01-tree-expansion.md` |
| [02 Cross-Reference Audit](../prompts/02-cross-reference-audit.md) | Your tree and documents may disagree, or you want verification before expansion | `review-cards/02-cross-reference-audit.md` |
| [03 Find a Grave Sweep](../prompts/03-findagrave-sweep.md) | You have deceased ancestors with enough death or burial context to search memorials | `review-cards/03-findagrave-sweep.md` |
| [04 GEDCOM Completeness](../prompts/04-gedcom-completeness.md) | You want to export or compare a GEDCOM file against your vault | `review-cards/04-gedcom-completeness.md` |
| [05 Source Citation Audit](../prompts/05-source-citation-audit.md) | You want to know which people or claims are under-sourced | `review-cards/05-source-citation-audit.md` |
| [06 Unresolved Persons](../prompts/06-unresolved-persons.md) | Documents mention unknown relatives, witnesses, neighbors, or informants | `review-cards/06-unresolved-persons.md` |
| [07 Timeline Gap Analysis](../prompts/07-timeline-gap-analysis.md) | A person has missing life events where records should probably exist | `review-cards/07-timeline-gap-analysis.md` |
| [08 Open Question Resolution](../prompts/08-open-question-resolution.md) | You have explicit questions in `Open_Questions.md` and want focused resolution | `review-cards/08-open-question-resolution.md` |
| [09 Local History Extraction](../prompts/09-bygdebok-extraction.md) | You have digitized local histories, bygdeboker, village books, or county histories | `review-cards/09-bygdebok-extraction.md` |
| [10 Colonial Records Search](../prompts/10-colonial-records-search.md) | You are researching pre-1800 American lines with sparse vital records | `review-cards/10-colonial-records-search.md` |
| [11 Immigration Search](../prompts/11-immigration-search.md) | You need passenger lists, border crossings, naturalization records, or origin clues | `review-cards/11-immigration-search.md` |
| [12 DNA Chromosome Analysis](../prompts/12-dna-chromosome-analysis.md) | You have segment data and want leads that stay separate from documentary proof | `review-cards/12-dna-chromosome-analysis.md` |

## Risky States

| State | Do first | Why |
|---|---|---|
| Living-person-heavy tree | [Privacy Mode](privacy-mode.md) | Public AI tools should not receive private living-person details |
| No source files | `checklists/first-week-checklist.md` | AI needs known facts and source labels before it can help safely |
| Known contradictions | `prompts/02-cross-reference-audit.md` | Expansion can spread mistakes through the tree |
| DNA-only interpretation | `guides/bundles/dna-pack.md` | DNA suggests leads, it does not identify a specific ancestor by itself |
