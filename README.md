# TRACE-CU Evaluation Statistics and Supplementary Materials

This repository accompanies the TRACE-CU manuscript and provides pseudonymized statistical records for verifying the reported evaluation summaries, confidence intervals, paired comparisons, and failure counts.

## Public Scope

The public package contains pseudonymized evaluation counts and statistical outputs. It does not contain complete-corpus structured extraction results, complete gold-standard records, publication abstracts, expert annotations, adjudication workbooks, complete prompts, repair templates, source code, API credentials, raw model responses, model reasoning traces, or figure assets.

The 90 held-out publications are represented by stable public identifiers `EVAL001` through `EVAL090`. The files `splits/development_10_pmids.csv` and `splits/heldout_90_pmids.csv` list the 10 development and 90 held-out PMIDs, respectively. The PMID sets do not provide a mapping from the public EVAL identifiers to individual PMIDs. That crosswalk remains excluded.

## Gold-Standard Access

The adjudicated gold-standard annotations are not available for unrestricted public download. They are available from the corresponding author upon reasonable request, together with the annotation guideline for the supplied dataset version. The authors have chosen request-based distribution so that an identified annotation version and its associated guideline are provided together.

This is an author-selected access policy, not a legal, copyright, or participant-privacy restriction claimed for the publicly accessible source literature. Complete individual expert annotations and adjudication workbooks are not included in the public package. Requests for Gold and its guideline should be directed to the corresponding author identified in the manuscript.

## Contents

| Directory | Public contents |
|---|---|
| `splits/` | Development (10) and held-out (90) PMID lists |
| `documents/` | Archived Supplementary Materials 1-5 in DOCX format |
| `evaluation/summary_metrics/` | Point estimates, class-level PIO metrics, 95% confidence intervals, and paired comparisons |
| `evaluation/publication_level/` | Pseudonymized publication-level count workbooks for Tables 3-5 |
| `evaluation/bootstrap/` | Publication-level bootstrap distributions |
| `evaluation/failure_analysis/` | Aggregate failure counts and 53 pseudonymized CU-level failure records |

The five repository documents retain their existing filenames. Their topics correspond to Multimedia Appendices 4-8 in the third-round revision. Updated journal appendices are supplied with the manuscript; this repository update does not replace the archived DOCX files.

## Evaluation Scope

- Held-out evaluation publications: 90
- Adjudicated gold-standard CUs in the held-out evaluation: 241
- Public identifiers: `EVAL001-EVAL090`
- Bootstrap resampling unit: publication
- Bootstrap iterations: 2,000
- Random seed: 20260625
- Full TRACE-CU CU counts: TP=232, FP=27, FN=9
- Correct logical binding among matched CUs: 214 of 232

The public workbooks retain only metric numerators and denominators. They do not disclose the clinical content of gold or predicted CUs.

## Verifying the Reported Statistics

1. Sum the publication-level count columns within each worksheet in `evaluation/publication_level/`.
2. Recalculate the point estimates using the metric definitions in Supplementary Material 3.
3. Use the distributions in `evaluation/bootstrap/` to verify the percentile 95% confidence intervals and paired comparisons.
4. Compare the resulting values with `evaluation/summary_metrics/` and Supplementary Material 3.

## Failure Statistics

Supplementary Material 5 reports 53 distinct CU-level failure records. The pseudonymized `02_failure_cu_records.csv` provides the corresponding count encodings and concise English reasons without publication text or complete CU content. Aggregate failure categories are provided in `01_failure_summary.csv`.

## Citation and Versioning

Cite the immutable commit URL containing the files used. No release tag is claimed. Earlier commits do not include files added in subsequent updates; the development and held-out lists are included in the commit that adds the splits directory.

## License

The released documentation and statistical data are licensed under the Creative Commons Attribution 4.0 International License. See `LICENSE.md`.
