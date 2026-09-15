# Held-Out Evaluation Failure Analysis

This directory documents failure modes observed in the same 90-publication held-out evaluation set and 241 adjudicated gold-standard comparison units used for the principal TRACE-CU performance analysis.

## Files

- `01_failure_summary.csv`: aggregate CU-level failure categories and comparison-structure counts.
- `02_failure_cu_records.csv`: 53 anonymized machine-readable CU-level failure records with concise English remarks.

Five representative failure scenarios are reported in Supplementary Material 5. The complete internal audit workbook, publication abstracts, and duplicate case export are not included in the public package.

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

The legacy scope-exclusion analysis is not included because it concerns publications outside the evaluation scope rather than extraction failures. These records support error characterization and do not replace the primary performance tables.
