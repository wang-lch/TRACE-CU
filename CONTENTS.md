# Package Contents

## Journal Appendices

Multimedia Appendices 1-8 are submitted with the manuscript. No duplicate appendix DOCX or PDF files are included in this repository.

## Documentation and License

- `README.md`: public scope, data access, evaluation scope, and arithmetic reproducibility.
- `CONTENTS.md`: package file directory.
- `LICENSE.md`: license for the released documentation and statistical data.
- `evaluation/README.md`: statistical file organization and bootstrap settings.
- `evaluation/failure_analysis/README.md`: failure-record definitions, denominators, and interpretation.
- `.gitignore`: exclusions for local system files, credentials, and runtime artifacts.

## Publication Lists

- `splits/development_10_pmids.csv`: 10 development publications.
- `splits/heldout_90_pmids.csv`: 90 held-out publications.

## Publication-Level Count Workbooks

- `evaluation/publication_level/01_table3_pio_counts.xlsx`: three PIO method worksheets.
- `evaluation/publication_level/02_table4_method_counts.xlsx`: nine method worksheets.
- `evaluation/publication_level/03_table5_registry_ablation_counts.xlsx`: four registry-input worksheets.

All publication identifiers in these workbooks use `EVAL001-EVAL090`.

## Summary Metrics

- `evaluation/summary_metrics/01_table3_pio_point_estimates.csv`
- `evaluation/summary_metrics/02_table3_pio_bootstrap_ci.csv`
- `evaluation/summary_metrics/03_table3_pio_paired_comparisons.csv`
- `evaluation/summary_metrics/04_tables4_5_point_estimates.csv`
- `evaluation/summary_metrics/05_tables4_5_bootstrap_ci.csv`
- `evaluation/summary_metrics/06_tables4_5_paired_comparisons.csv`

## Bootstrap Records

- `evaluation/bootstrap/01_table3_pio_bootstrap_distributions.csv`
- `evaluation/bootstrap/02_tables4_5_bootstrap_distributions.csv`

## Failure Statistics

- `evaluation/failure_analysis/01_failure_summary.csv`
- `evaluation/failure_analysis/02_failure_cu_records.csv`

Illustrative cases are described in Multimedia Appendix 8 supplied with the manuscript and are not duplicated as a separate case file here. The failure files contain count summaries and record-level scoring classifications with English explanations.

## Excluded From Public Release

The package excludes complete-corpus structured outputs, complete gold-standard records, publication abstracts, mappings between PMIDs and EVAL identifiers, expert annotation files, adjudication workbooks, complete prompts, raw model responses, source code, and figure assets.
