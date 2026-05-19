# Normie Usability Layer

**Goal:** Turn `autoresearch-genealogy` from a useful prompt library into a guided kit a nontechnical family researcher can use without understanding repos, prompt design, or genealogy methodology upfront.

**Architecture:** Keep the core repository markdown-first. Add a beginner entry point, prompt picker, workflow bundles, checklists, review cards, fixture walkthrough, and plain-language reference layer. The existing prompts stay as the power-user substrate; the new layer tells users what to run, when to run it, what to trust, and what to review.

**Tech Stack:** Markdown, Ruby validator, existing fixtures, no web app in MVP.

## Decisions

| Decision | Default | Why |
|---|---|---|
| Primary audience | Nontechnical family researcher with documents, family stories, or DNA results | This is the highest-friction audience and forces clarity |
| Delivery format | Markdown-first, repo-native | Avoids adding app complexity before the content path is proven |
| First screen | `START_HERE.md` | Most users need sequencing before they need prompts |
| Prompt packaging | Bundles plus picker | Reduces choice overload while preserving expert access |
| Safety posture | Privacy-first and source-first | Genealogy errors and living-person leaks are the main harms |
| Example data | One fictional family fixture reused everywhere | Keeps onboarding coherent and privacy-safe |

## Spec Breakdown

| # | Spec | Description | Depends On | MVP |
|---|---|---|---|---|
| 01 | Start Here | One-page entry point with paths by user situation. | - | Yes |
| 02 | Prompt Picker | Decision tree that maps current state to the next prompt. | 01 | Yes |
| 03 | Prompt Bundles | Beginner, document, DNA, verification, and advanced packs. | 02 | Yes |
| 04 | Checklists | Printable/checkable workflows for common nontechnical tasks. | 01 | Yes |
| 05 | Human Review Cards | Per-prompt acceptance checks and common failure modes. | 02 | Yes |
| 06 | Fictional Walkthrough | End-to-end demo using the minimal fixture vault. | 03, 05 | Yes |
| 07 | Plain-Language Reference | Translate source/evidence concepts into normie language. | 04, 05 | Yes |
| 08 | Obsidian-Lite Setup | Explain Finder/Markdown usage without Obsidian. | 01 | Yes |
| 09 | Privacy Mode | Public AI prompt safety, redaction, and sharing guidance. | 01 | Yes |
| 10 | Optional Static Site | A simple generated docs site after markdown flow is proven. | 01-09 | No |

## Interface Summary

- `START_HERE.md` links to `guides/prompt-picker.md`, `guides/bundles/*.md`, `checklists/*.md`, and `walkthroughs/first-run.md`.
- Prompt bundles consume existing `prompts/*.md`; they do not duplicate full prompt text.
- Human review cards live beside prompts in `review-cards/` and are linked from bundles.
- The fictional walkthrough consumes `fixtures/minimal-vault/` and `fixtures/golden-runs/`.
- Validator gains checks for required usability files once each spec is implemented.

## MVP Definition

The MVP is complete when a user who only knows “I have names, photos, and DNA results” can:

1. Open `START_HERE.md`.
2. Choose a path in under 2 minutes.
3. Copy the right prompt or bundle.
4. Know what files to prepare.
5. Know what output should look like.
6. Know what not to trust.
7. Avoid exposing living-person details.

## Out Of Scope For MVP

- Web app or hosted documentation site.
- Interactive CLI wizard.
- Automated genealogy database scraping.
- Real user data examples.
- Paid database integrations.
- Full behavior test harness for all prompts.
