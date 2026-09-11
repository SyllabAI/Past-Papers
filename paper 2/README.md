# paper 2 — Edexcel IGCSE Chemistry Paper 2C (GLM-OCR markdown corpus)

One folder per exam sitting; each contains the question paper and/or mark scheme
(as converted so far) plus the figures both reference.

```
paper 2/
  <year>-<Mon>[-R]/        e.g. 2012-Jan, 2013-Jun-R, Specimen-2017
    QP.md                  question paper (GLM-OCR markdown, links rewritten to local assets)
    MS.md                  mark scheme (same treatment)
    assets/                figures referenced by QP.md / MS.md (local copies)

  MANIFEST.json            full provenance: original filenames, source URLs,
                           sha256, sizes, formats, per-image referencing docs
```

**Sessions:** 41 (Specimen-2017 ... 2024-Jun-R); 41 with QP,
41 with MS. Missing docs correspond to conversions not yet run.

**Images:** 1227 local copies; every batch so far downloaded with zero failures.

## Provenance & expiry

Images are local copies of signed OCR-service URLs that expire roughly one week after
conversion. Original URLs are preserved per-image in MANIFEST.json; the local copies
are the durable artifacts.

Barcode, logo and page-furniture crops were deliberately excluded by the OCR conversion -
the md reference set is the wanted set.

Near-duplicate conversions are documented under sessions[slug].superseded_duplicates
(alternates remain recoverable from git history).

## Qualification codes

Sessions before 2019 are expected to be spec 4CH0 (A*-G) and 2019+ spec 4CH1 (9-1).
Confirm against the paper covers before tagging curriculum identities.

## Next step

Feed each complete session to the parser bridge:

```
syllabai-glmocr-pair <session>/QP.md <session>/MS.md <out-dir>
```
