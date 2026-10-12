# Held-Out Evaluation Failure Analysis

This directory contains failure-count summaries and scoring classifications associated with the 90-publication evaluation set and 241 reference CUs. The records include FP, FN, and binding-error count contributions, with category definitions and interpretation provided in Multimedia Appendix 8.

## Files

- `01_failure_summary.csv`: aggregate CU-level, numerical/state, and evidence-support failure categories.
- `02_failure_cu_records.csv`: 53 pseudonymized machine-readable CU-level failure records with concise English remarks.

Illustrative cases and the interpretation of scoring records are described in Multimedia Appendix 8 supplied with the manuscript. The complete internal audit workbook, publication abstracts, and duplicate case export are not included in the public package.

## Denominators

- Gold-standard CUs: 241
- Matched predicted-gold CU pairs: 232
- False-positive CUs: 27
- False-negative CUs: 9
- Fully correct matched CU pairs: 214
- Matched-CU logical-binding errors: 18
- Distinct CU-level failure records: 53

One unresolved multi-arm mapping contributed both one false-positive and one false-negative event. The 53 records therefore represent 54 CU-detection or logical-binding error events.

Numerical/state and evidence-support failures use separate eligible-item denominators and must not be added to the CU-level failure count.

## Scope Boundary

Excluded candidate-record classifications are not included in the retained-prediction failure table. They do not identify a separate cohort of publications outside the 90-publication evaluation set. The scoring classifications do not establish runtime validation dispositions or manual-review workload.

## Interpretation of Record Labels

- The 53 records concern 22 pseudonymized publications and encode 54 events: 27 FP, 9 FN, and 18 matched-CU binding errors.
- Structure labels come from the prediction/review archive, not a reclassification by the gold-standard strata in Multimedia Appendix 3.
- An unmatched prediction or reference CU is a reference-relative scoring outcome; it does not automatically establish a fabricated clinical statement or an explicitly reported omitted pairwise comparison.
- Arm-order disagreement records do not, by themselves, prove an inverted clinical effect.
- Statistical-field misattribution in the CU categories refers to mean differences placed in the HR/OR field, not overall P values assigned to specific contrasts.
- Validation interception, runtime dispositions, and manual-review workload cannot be inferred from these scoring columns.
- The numerical/state and evidence-support breakdowns report aggregate item-code counts. Source-linked annotations for individual numerical/state and evidence-support items are not included in this package.

## Columns

`eval_id` is the pseudonymized publication identifier. `gold_ref` and `prediction_ref` are within-publication record references; an empty reference indicates no corresponding record on that side. `failure_category` is the primary scoring classification. `comparison_structure` is the recorded prediction/review label. `cu_fp`, `cu_fn`, and `cua_error` are count contributions, each 0 or 1. `remarks` explains the recorded discrepancy and its interpretive limits.
