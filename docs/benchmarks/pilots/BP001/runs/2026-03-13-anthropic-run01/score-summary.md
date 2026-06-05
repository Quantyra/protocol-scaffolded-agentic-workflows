# Anthropic BP001 Run 01 Score Summary

## Stronger condition
- Taught-protocol condition

## Baseline total
- `1/10`

## Taught total
- `8/10`

## Main observed differences
- The baseline output hallucinated a completely different repository structure and fake tool calls.
- The taught output adopted the planning protocol structure, added validation checkpoints, artifact retention, and a clear comparison condition.
- The taught output still reframed the repo as a generic teaching-system implementation target instead of the current benchmark-execution phase.

## Confounds
- Same-operator scoring
- The taught prompt embeds the planning protocol directly
- The taught output was captured in concise form after a shorter-token rerun
- The retained baseline artifact is an operator narrative rather than a full verbatim transcript; see `baseline-verbatim-retention-gap.md`

## Interpretation
This is evidence that Anthropic `claude-sonnet-4-6` improved materially under the taught planning protocol on BP001, but the magnitude should be interpreted cautiously because the baseline failed catastrophically and is retained as an operator narrative rather than a verbatim transcript. Task alignment still needs monitoring.

## Follow-on action
- Execute Anthropic BP002 and compare whether task drift persists under workflow constraints.
