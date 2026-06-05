# Visual Render QA: EMSE Packet V1.0.7

Date: 2026-06-05

## Scope

This note records the final visual QA pass for the EMSE upload packet after the Claude major-revision feedback pass and artifact release metadata bump to `v1.0.7`.

Checked documents:

- `upload-set/EMSE_main_manuscript.docx`
- `upload-set/EMSE_title_page_and_declarations.docx`
- `upload-set/EMSE_cover_letter.docx`
- `upload-set/EMSE_supplement_source.docx`
- `upload-set/ESM_1.pdf`

## Render Method

The bundled LibreOffice render path was not available on this workstation. The DOCX files were exported to PDF with local Word automation, then rasterized with `pdftoppm` into page PNGs and contact sheets.

Final render evidence:

- `word-pdf-render-v1.0.7/`
- `page-renders-v1.0.7/`

## Result

The final contact sheets were visually inspected. Pages are present, tables fit within the page body, headings and body text are readable, and no clipping, overlap, missing title block, missing release reference, or page-break failure was observed.

Text checks also confirmed that the main manuscript contains the revised title, `v1.0.7` release reference, instruction-specificity caveat, and single-run measurement caveat. The supplement PDF contains the 2026-06-05 date, instruction-specificity note, replication and variance note, and the `v1.0.7` release URL.

## Remaining Limitation

This QA pass verifies layout and metadata consistency for the regenerated submission packet. It does not resolve the Anthropic BP001 baseline verbatim transcript retention gap, which is separately documented in `docs/benchmarks/pilots/BP001/runs/2026-03-13-anthropic-run01/baseline-verbatim-retention-gap.md`.
