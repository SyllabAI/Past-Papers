# GLM-OCR Markdown Sample Corpus

**Corpus location:** `Past-Papers/GLM-markdown-sample/`
**Recorded:** 2026-09-05 (Session 8 corpus audit)
**Sample count:** 6 Markdown files = 3 complete QP/MS pairs
**Converter:** Z.ai GLM OCR (Markdown export)
**Export timestamps (in file names):** 2026-03-31 17:15–17:16
**Committed:** 2026-09-04 (commit `4a19b3a`, "Add")

## File inventory

| File | Lines | Kind | Exam identity (from document content) |
|---|---|---|---|
| `June 2025 (IAL) QP-2026-03-31_17-16-10.md` | 721 | QP | Pearson Edexcel IAL Physics **WPH11/01** "Mechanics and Materials", Summer 2025, 80 marks |
| `June 2025 (IAL) MS-2026-03-31_17-16-12.md` | 240 | MS | Same paper — Mark Scheme (Results), log number `P78753A`, publication code `WPH11_01_2506_MS` |
| `October 2025 - Unit 1 QP-2026-03-31_17-16-04.md` | 713 | QP | Pearson Edexcel IAL Physics **WPH11/01**, October 2025, 80 marks |
| `October 2025 - Unit 1 MS-2026-03-31_17-16-07.md` | 157 | MS | Same paper — log number `P78831A`, publication code `WPH11_01_2510_MS` |
| `October 2025 - Unit 1A QP-2026-03-31_17-15-58.md` | 912 | QP | Pearson Edexcel IAL Physics **WPH11/01A** (variant with answer book), Wed 8 Oct 2025 afternoon, 1 h 30 min, 120 marks |
| `October 2025 - Unit 1A MS-2026-03-31_17-16-01.md` | 177 | MS | Same paper — log number `P87440A`, publication code `WPH11_01A_2510_MS` |

Naming convention: `<session label> [<- unit label>] QP|MS-<export-date_time>.md`.
The QP/MS pairing is expressed only through the shared session/unit label and matching
paper references inside the documents; there is no machine-readable pair manifest in
this repository.

## Image assets — READ BEFORE USING THIS CORPUS

**This folder contains no image binaries.** Every image reference inside the Markdown
files is an HTML tag of the form:

```html
<div style='text-align: center;'><img src='https://maas-watermark-prod-new.cn-wlcb.ufileos.com/ocr%2Fcrop%2F<session-id>%2Fcrop_<n>_<millis>.png?UCloudPublicKey=...&Signature=...&Expires=<epoch>' alt='OCR图片'/></div>
```

These are **signed, expiring URLs** to a UCloud object store. Audited on 2026-09-05:

- every checked URL returns **HTTP 401** — the `Expires` epoch values resolve to
  **2026-04-07**, roughly one week after the 2026-03-31/04-01 export;
- therefore **the images referenced by this corpus are currently unrecoverable from
  the Markdown source**; the crops exist only inside Z.ai's OCR export history;
- the alt text is the fixed Chinese string `OCR图片` ("OCR image") — it carries no
  per-image semantics.

Reference counts: June QP 74 refs, October Unit 1 QP 74, October Unit 1A QP 77,
June MS 1, October MS 0. The referenced images include **page furniture** (cover
pages, answer boxes, blank-page artefacts) interleaved with **semantic figures**
(diagrams, graphs, apparatus) — the reference stream does not distinguish them.

If faithful visual rendering of these three papers is required, the OCR export
must be repeated with images saved locally. Until then this corpus is usable as a
**text/structure** sample (questions, parts, marks, tables, equations, mark-scheme
semantics), not as a visual-asset sample.

## Related but separate: orphaned OCR crops

`IAL/Edexcel/Physics/Unit 4/` contains 10 PNG files named
`ocr_crop_20260709013610e74b664078f24ba5_crop_<n>_<millis>.png`
(one shared session id, generated 2026-07-09). These are real, readable image
binaries (258×413 … 1398×894 px, 11–212 KB), but **no Markdown file in this
repository references them** and no Markdown counterpart for that OCR session was
committed. They are currently orphaned assets.

## Corpus history

- 2026-03-19: an earlier GLM OCR batch was committed **inside** the per-paper
  directories (e.g. `IAL/Edexcel/Physics/Unit 1/January 2009 MS - ... .md`).
- 2026-08-08 (commit `d198223`): those old `.md` files were deleted
  ("Delete old .md files").
- 2026-09-04 (commit `4a19b3a`): the current clean 6-file sample folder was added.

## Usage rules (SyllabAI content pipeline)

1. Do not re-OCR this corpus unnecessarily; treat the Markdown as the presentation
   source and normalize it into the canonical document format
   (see `syllabai-parser/docs/glm-ocr/`).
2. Preserve file provenance: the original PDFs for these sessions exist elsewhere
   in this repository where available; the Markdown is a derived representation.
3. The syntax of these files is documented evidence-first in
   `syllabai-parser/docs/glm-ocr/real-corpus-syntax-report.md`; changes to the
   corpus (re-export with images, new files) should update that report.
