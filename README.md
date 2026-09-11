# Past-Papers — SyllabAI corpus repo

Official Edexcel past-paper content (QP = question paper, MS = mark scheme) for
IGCSE Chemistry, plus GLM-OCR markdown conversions prepared for the SyllabAI
content pipeline.

## Organized folders

| Folder | Contents |
|---|---|
| `paper 1/` | Paper 1C — 41 sessions (Jun 2011 → Jun 2024 + Specimen 2017), per-session layout, 2,002 preserved figures |
| `paper 2/` | Paper 2C — 19 sessions (Jun 2011 → Jan 2023 (R)), per-session layout, 573 preserved figures |
| `IAL/`, `IGCSE/` | Raw official QP/MS PDF archive (by qualification/board/subject/unit) |
| `GLM-markdown-sample/` | First GLM-OCR sample batch + audit README (Session 8) |

## Per-session layout (paper 1 & paper 2)

```
<year>-<Mon>[-R]/     e.g. 2012-Jan, 2013-Jun-R, Specimen-2017
  QP.md               question paper (GLM-OCR markdown, links rewritten to local assets)
  MS.md               mark scheme   (same treatment)
  assets/             figures referenced by QP.md / MS.md (local copies of expiring OCR URLs)
MANIFEST.json         full provenance: original filenames, source URLs, sha256, per-image referencing docs
README.md             paper-specific conventions and session table
```

Original signed image URLs expire (paper 1 ≈ 2026-09-17, paper 2 ≈ 2026-09-18);
the local copies and the manifests are the durable record. Barcode / page-furniture
crops were deliberately excluded by the OCR conversion — md references are the
wanted set.

## Next step

Feed each session to the parser bridge in `syllabai-parser`:

```
syllabai-glmocr-pair <session>/QP.md <session>/MS.md <out-dir>
```
