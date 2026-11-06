# Portfolio revision

This edition is based on MiniProject2.ipynb and the supplied Armenian_COVID_Data.csv. It is a distinct revision; the original uploaded files were not overwritten.

## Correctness and reproducibility

- Replace the expired signed download URL with a local CSV path.
- Validate schema, date format, counts, duplicates and calendar coverage.
- Treat non-monotonic reported counts as daily under an explicit, source-verification caveat; remove the original differencing step.
- Keep missing dates unknown; do not fill missing lag values with zero.
- Preserve count units for analysis and target evaluation.
- Create the next-calendar-day target once.
- Fit preprocessing inside a training pipeline, not on the full dataset.
- Use chronological cross-validation with a gap instead of ordinary folds.
- Add persistence, training-mean and Linear Regression baselines.
- Keep Random Forest as the submitted notebook's model and tune within training only.
- Select by training-only validation MAE; reserve the last period for final reporting.
- Recompute charts, correlations, predictions and metrics; do not reuse the slides' values.
- Explain correlation limitations, temporal gaps and weak forecasting results.

## Provenance

The notebook and presentation describe different model experiments. The original presentation's KNN, Polynomial Regression and Decision Tree results are not implemented or reproduced here because their corresponding code was not supplied. The additional Linear Regression and baselines in this edition are new comparisons, not a reconstruction of the slide experiment. Team attribution follows the original presentation.

## Validation performed

All seven code cells were executed in order in one Python process with real captured table and figure outputs. The notebook passed nbformat schema validation. Exported charts were visually reviewed. A separate Jupyter server/kernel could not start in the execution environment, so GUI-based Restart and Run All was not verified. No model metrics were manually inserted into notebook outputs.
