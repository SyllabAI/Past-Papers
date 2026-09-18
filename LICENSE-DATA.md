# LICENSE-DATA — Data Licensing & Provenance Notice

**Added:** 2026-09-15 (documentation audit reconciliation, audit item D9)
**Scope:** the corpus content in this repository. The repository's own tooling and scripts are code and follow the repository license; this notice covers the collected/derived content.

## What this repository contains

Raw, operator-collected Edexcel past-paper question papers and mark schemes (QP/MS PDFs), staged pre-normalization. This is the ingestion source feeding the normalized, charter-governed corpus in `SyllabAI/syllabai-pastpapers`; no application code lives here. (The early GLM-OCR markdown samples used to bootstrap the parser were removed 2026-09-15 as superseded by that normalized corpus.)

## Source and provenance

- Examination material © Pearson Education Ltd (Edexcel); revision-note content derived from Save My Exams material © Save My Exams Ltd, with source URLs preserved in each note's YAML front-matter (capture date + provenance tier). All of it is used for a non-commercial, educational course project (an adaptive-learning research pilot for ~50 students); no commercial use is made of this content and no ownership is claimed.
- Provenance is machine-checkable: SHA-256 checksums, manifests and ledgers accompany the material (see the corpus manifests and `MANIFEST.json` / per-paper `manifest.yaml` records).

## Licensing position

- Internal pilot use under institution/own-use terms (ADR-013 posture). Re-check terms before any redistribution — redistribution is **not** authorized by this notice.
- Takedown / correction requests: open an issue on this repository or contact the repository owner via GitHub; affected material will be removed promptly.

## Related internal policy

- `SyllabAI/syllabai` → ADR-013 (license wall), `PROJECT_CONTEXT.md` (Approved technology direction — license wall), and the corpus charter in `syllabai-pastpapers` (README).
