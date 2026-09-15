# TRACE-CU Evaluation Statistics and Supplementary Materials

This repository accompanies the TRACE-CU manuscript and provides anonymized statistical records for verifying the reported evaluation summaries, confidence intervals, paired comparisons, and failure counts.

## Public Scope

The public package contains anonymized evaluation counts and statistical outputs. It does not contain complete-corpus structured extraction results, complete gold-standard records, publication abstracts, expert annotations, adjudication workbooks, complete prompts, API credentials, raw model responses, model reasoning traces, or figure assets.

The 90 held-out publications are represented by stable public identifiers `EVAL001` through `EVAL090`. PMID mappings and development-set identifiers are not included in this release.

## Contents

| Directory | Public contents |
|---|---|
| `documents/` | Supplementary Materials 1-5 in DOCX format |
| `evaluation/summary_metrics/` | Point estimates, class-level PIO metrics, 95% confidence intervals, and paired comparisons |
| `evaluation/publication_level/` | Pseudonymized publication-level count workbooks for Tables 3-5 |
| `evaluation/bootstrap/` | Publication-level bootstrap distributions |
| `evaluation/failure_analysis/` | Aggregate failure counts and 53 anonymized CU-level failure records |

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

Supplementary Material 5 reports 53 distinct CU-level failure records. The anonymized `02_failure_cu_records.csv` provides the corresponding count encodings and concise English reasons without publication text or complete CU content. Aggregate failure categories are provided in `01_failure_summary.csv`.

## Citation and Versioning

Use the immutable GitHub release tag and commit identifier associated with this package. The initial release is designated `v1.0.0`.

## License

The released documentation and statistical data are licensed under the Creative Commons Attribution 4.0 International License. See `LICENSE.md`.
