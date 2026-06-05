# Anthropic BP001 Baseline Verbatim Retention Gap

Date recorded: 2026-06-05

## Summary

The retained `baseline-plan.md` for this run is an operator-side narrative summary of the baseline output, not a full verbatim transcript.

This is a reproducibility limitation because the run also carries the largest hosted `BP001` delta in the manuscript spine:

- baseline: `1/10`
- taught: `8/10`

## Current use rule

Use this run as evidence that the retained operator-side scoring observed catastrophic baseline drift, but do not let this run carry the hosted planning claim by itself.

Any manuscript-facing interpretation should state that the Anthropic `BP001` baseline has a weaker transcript-retention surface than the OpenAI and Google hosted baselines.

## Search performed

On 2026-06-05, the following locations were searched for a fuller raw transcript using the specific BP001 Anthropic baseline signatures, including `list_directory`, `/pyproject.toml`, `/app/api/v1/endpoints/auth.py`, and `/app/services/document_service.py`:

- local public artifact workspace: `C:\Users\Dan\Desktop\Projects\Quantyra-Teaching-Artifacts`
- local active Teaching workspace: `C:\Users\Dan\Desktop\Projects\Quantyra-Teaching`
- Git history for the public artifact repository, including the original `dfredriksen` namespace history now transferred to `Quantyra/protocol-scaffolded-agentic-workflows`
- GitHub repository lookups for the old `dfredriksen/protocol-scaffolded-agentic-workflows` and `dfredriksen/quantyra-teaching-artifacts` names

Result: the searches found the same retained `baseline-plan.md` summary in the local workspaces and across Git history. No separate `baseline-raw-output.md`, `raw-response.txt`, conversation transcript, or equivalent BP001 Anthropic baseline transcript was found in those sources.

## Required future handling

Future baseline and taught runs must preserve verbatim output transcripts, not only operator narratives or summaries.
