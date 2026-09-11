# paper 1 — Edexcel IGCSE Chemistry Paper 1C (GLM-OCR markdown corpus)

One folder per exam sitting; each contains the question paper, its mark scheme,
and the figures referenced by both.

```
paper 1/
  <year>-<Mon>[-R]/        e.g. 2012-Jan, 2013-Jun-R, Specimen-2017
    QP.md                  question paper (GLM-OCR markdown)
    MS.md                  mark scheme (GLM-OCR markdown)
    assets/                images referenced by QP.md / MS.md (local copies)

  MANIFEST.json            full provenance: original filenames, source URLs,
                           sha256, sizes, formats, per-image referencing docs
```

**Sessions:** 41 (Specimen-2017 … 2024-Jun-R), all with complete QP+MS pairs.
**Images:** 2002 local copies, zero failures.

## Provenance & expiry

Images were downloaded from signed OCR-service URLs that expire (paper 1 around 2026-09-17, paper 2 around 2026-09-18). The original URLs are kept in
`MANIFEST.json` for traceability; the local copies are the durable artifacts.

Barcode, logo and page-furniture crops were deliberately excluded by the OCR conversion —
the md reference set is the wanted set; nothing else needs rescuing.

## Qualification codes

Sessions before 2019 are expected to be spec **4CH0** (A*-G) and 2019+ spec **4CH1** (9-1).
Confirm against the paper covers before tagging curriculum identities.

## Next step

Feed each session to the parser bridge:

```
syllabai-glmocr-pair <session>/QP.md <session>/MS.md <out-dir>
```
