# TRACE-CU Data and Statistical Archive

This repository accompanies the TRACE-CU manuscript and contains publication lists and retained count-based statistical materials.

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
| `evaluation/summary_metrics/` | Point estimates, class-level PIO metrics, 95% confidence intervals, and paired comparisons |
| `evaluation/publication_level/` | Pseudonymized publication-level count workbooks for Tables 3-5 |
| `evaluation/bootstrap/` | Publication-level bootstrap distributions |
| `evaluation/failure_analysis/` | Aggregate failure counts and 53 pseudonymized CU-level failure records |

Multimedia Appendices 1-8 are submitted with the manuscript and are not duplicated in this repository. The former Supplementary Materials 1-5 correspond to journal Multimedia Appendices 4-8. Their older DOCX copies have been removed from the current repository tree; earlier commits retain the historical versions.

The package contains publication-level count matrices and bootstrap distributions for the statistical summaries in Multimedia Appendix 6. Failure categories, count encodings, and English record explanations correspond to the scoring classifications described in Multimedia Appendix 8.

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

## Checking Arithmetic Reproducibility

1. Sum the publication-level count columns within each worksheet in `evaluation/publication_level/`.
2. Recalculate the point estimates using the metric definitions in Multimedia Appendix 6 supplied with the manuscript.
3. Use the distributions in `evaluation/bootstrap/` to verify the percentile 95% confidence intervals and paired comparisons.
4. Compare the resulting values with `evaluation/summary_metrics/` and Multimedia Appendix 6 supplied with the manuscript.

## Failure Statistics

Multimedia Appendix 8 supplied with the manuscript describes the CU-level scoring records and illustrative cases. The pseudonymized `02_failure_cu_records.csv` provides the corresponding count encodings and concise English reasons without publication text or complete CU content. Aggregate failure categories are provided in `01_failure_summary.csv`.

## Citation and Versioning

Cite the immutable commit URL containing the files used. No release tag is claimed. Earlier commits do not include files added in subsequent updates; the development and held-out lists are included in the commit that adds the splits directory.

## License

The released documentation and statistical data are licensed under the Creative Commons Attribution 4.0 International License. See `LICENSE.md`.
