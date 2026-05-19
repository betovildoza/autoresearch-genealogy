# DNA Chromosome Analysis

Analyze authorized local chromosome data cautiously, keeping genetic leads separate from documentary proof.

## Inputs To Replace

- `[VAULT_PATH]`: path to the genealogy vault folder
- `[DNA_DATA_PATH]`: local path to a redacted or authorized ancestry composition export
- `[ANCESTRY-A]`: ancestry component used as a calibration example

## Autoresearch Configuration

**Goal**: Parse local, authorized per-chromosome ancestry composition data to identify cautious maternal or paternal leads, then map those leads to documented ancestor lines only when the paper trail supports the same relationship.

**Metric**: Number of chromosomes where the likely parental origin of each copy has been determined

**Direction**: Maximize

**Verify**: Count entries in `[VAULT_PATH]/Chromosome_Painting.md` where Copy 1 and Copy 2 have been assigned a likely parental origin.

**Guard**:
- Do not paste raw DNA files, match lists, kit IDs, or segment files into public AI tools.
- Use only local files the tester is allowed to analyze. Do not analyze another person's DNA or match details without consent.
- Redact living match names and identifiers. Use labels such as `Living Match A`.
- Do not recommend third-party raw DNA uploads unless the user has separately reviewed privacy, consent, retention, law-enforcement access, and relative-impact tradeoffs.
- Without a parent's DNA test, copy assignment is PROBABILISTIC, not definitive. Always note uncertainty.
- Do not over-interpret small segments (<5 cM). They may be noise.
- The X chromosome has special inheritance: males inherit X only from their mother. Use this as a calibration point.
- Do not conflate genetic ancestry with ethnic or national identity.

**Iterations**: 6

**Protocol**:

1. **Confirm authorization and privacy**: Before reading data, confirm `[DNA_DATA_PATH]` is local, authorized, and redacted for living matches. If not, stop and write a privacy note instead of analyzing.

2. **Parse the data**: Read the local ancestry composition CSV. For each chromosome (1 through 22, plus X), extract:
   - Copy 1 ancestry segments (start position, end position, ancestry label)
   - Copy 2 ancestry segments

3. **Analyze the X chromosome first** (if the subject is male):
   - Males inherit X only from their mother
   - Whatever ancestry appears on the X chromosome is 100% maternal
   - Use this as a calibration: if X is entirely [ANCESTRY-A], then [ANCESTRY-A] is at least partly maternal

4. **Identify clean separations**: Look for chromosomes where Copy 1 is predominantly one ancestry and Copy 2 is predominantly another. These are the most informative for parental assignment.

5. **Build the assignment table**: For each chromosome:
   - What ancestry dominates Copy 1?
   - What ancestry dominates Copy 2?
   - Which copy is likely maternal? (Cross-reference with X chromosome findings)
   - Confidence: High (clean separation) / Moderate (mixed) / Low (no clear pattern)

6. **Map to genealogy**: Using the parental assignments:
   - Which ancestry components are maternal? Compare against documented maternal ancestor lines.
   - Which are paternal? Compare against documented paternal ancestor lines.
   - Do the proportions make sense? (e.g., if the documented tree has 3 Scandinavian grandparents and 1 Eastern European, the genetic proportions should roughly reflect this)

7. **Analyze specific components**:
   - Count segments of each ancestry type
   - Many small segments = ancestry from many generations ago
   - Few large segments = ancestry from recent generations
   - A single large segment on one chromosome = likely from a specific recent ancestor

8. **Create the analysis file**: `[VAULT_PATH]/Chromosome_Painting.md` with:
   - Per-chromosome table (Copy 1 ancestry, Copy 2 ancestry, likely parent, confidence)
   - Summary of maternal vs paternal components
   - Mapping to documented ancestor lines only where documentary evidence supports the same branch
   - Open questions (unexpected segments, components that do not match the documented tree)
   - Privacy note confirming that living match identifiers and raw DNA data were not exposed publicly
