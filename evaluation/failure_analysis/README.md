# Held-Out Evaluation Failure Analysis

This directory retains the archived failure-count summaries and scoring classifications associated with the 90-publication evaluation set and 241 reference CUs. The statistical files are unchanged in this document-packaging update.

## Files

- `01_failure_summary.csv`: aggregate CU-level, numerical/state, and evidence-support failure categories.
- `02_failure_cu_records.csv`: 53 anonymized machine-readable CU-level failure records with concise English remarks.

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
