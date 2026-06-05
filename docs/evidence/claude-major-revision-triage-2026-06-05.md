# Claude Major-Revision Triage

Date: 2026-06-05
Scope: Teaching paper manuscript and public artifact repository

## Accepted as substantively relevant

### Instruction-specificity confound

Claude's central design critique is valid. The baseline prompt is weak and underspecified, while the taught prompt is longer, more specific, and aligned with the scoring rubric. The current design supports an operational claim about explicit protocol scaffolding versus weak prompting, not an isolated causal claim that the reusable protocol artifact itself accounts for the full effect.

Implemented response:

- softened abstract, discussion, conclusion, hosted-results interpretation, and threats table
- added an instruction-matched-control requirement to the supplement

### Single-run cells and no variance

This is a major validity limitation. The hosted matrix is repeated across providers/families, but each retained provider-by-family-by-condition cell is one scored run. One- and two-point deltas should not be treated as stable effects.

Implemented response:

- added explicit no-variance language to methodology, threats, discussion, and supplement
- reframed retained score differences as observations rather than statistical estimates

### Evaluator independence overstatement

Claude's critique is mostly correct. `L0/L1` scoring is operator-side and lists Codex as evaluator. The human `L2` memo is useful but is one internal evaluator, has lower absolute totals than operator-side taught scores, and does not score baseline and taught separately.

Implemented response:

- reframed human `L2` as directional support, not condition-level quantitative confirmation
- added explicit Codex/operator-side scoring language
- added same-family/self-judging caution for Anthropic `L2A`

### BP001 Anthropic transcript retention gap

The Anthropic `BP001` baseline artifact is an operator narrative rather than a full verbatim transcript. Because that run has the largest planning delta, it should not carry the hosted planning claim alone.

Implemented response:

- added `baseline-verbatim-retention-gap.md`
- updated the run score summary and manuscript threats table

### Metadata/version inconsistency

Claude correctly identified stale citation metadata. The repository had advanced releases beyond the manuscript's older fixed-release wording, and `CITATION.cff` contained a stale preferred-citation note.

Implemented response:

- fixed `CITATION.cff` preferred-citation title and note
- kept the current fixed release at `v1.0.7`

## Partly accepted, with pushback

### "This is not protocol-vs-no-protocol"

Accepted for causal identification. The current design does not isolate protocol reuse from instruction specificity.

Pushback: the operational comparison is still meaningful for software-engineering practice. Moving from underspecified prompting to explicit reusable protocol scaffolding is a real workflow intervention. The paper should claim that operational effect, not a fully isolated mechanism.

### Human `L2` evidence "leans harder than it can bear"

Accepted as a warning against overclaiming. The previous wording overstated how far the human memo closes evaluator independence.

Pushback: the human memo still has evidentiary value as a distinct reader's directional review and as a pressure test on score magnitude. It should remain in the paper, but with weaker language.

## Not fixable without new work

### Instruction-matched ablation

This cannot be fixed by editing. It requires new benchmark runs with a verbose, rubric-aligned non-protocol control condition.

### Replicated trials and variance

This cannot be fixed by editing. It requires repeated runs per provider/family/condition and revised reporting of variance or uncertainty.

### Full verbatim transcript for Anthropic BP001 baseline

This cannot be reconstructed honestly from current artifacts. The repo now records the retention gap rather than fabricating a transcript.

## Recommended next experimental work

1. Define an instruction-matched control prompt for `BP001` and `BP002`.
2. Run at least three repeats per hosted provider/condition on the highest-value benchmark families.
3. Use a human-review worksheet that separates baseline and taught condition scores.
4. Preserve full verbatim transcripts for every output.
5. Treat deltas of two points or less as descriptive unless supported by repeated-run stability.
