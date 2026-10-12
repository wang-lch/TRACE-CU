# Evaluation Statistics

This directory contains pseudonymized count matrices and count-derived statistical outputs corresponding numerically to manuscript Tables 3-5.

## Files by Level

1. `publication_level/`: publication-level count workbooks using `EVAL001-EVAL090` rather than PMID values.
2. `summary_metrics/`: point estimates, confidence intervals, and paired comparisons.
3. `bootstrap/`: 2,000-replicate publication-level bootstrap distributions.
4. `failure_analysis/`: aggregate failure counts and pseudonymized CU-level failure encodings.

All public matrices contain statistical counts only. Publication abstracts, complete gold and prediction content, and internal adjudication records are excluded.

The Table 3 workbook contains one worksheet per PIO method. The Table 4 and Table 5 workbooks contain one worksheet per reported method or input condition. Column totals reproduce the values in `summary_metrics/`.

Confidence intervals use publication-level percentile bootstrap resampling (2,000 replicates; seed 20260625). Paired differences use the same sampled publication indices for both conditions.
