# Model validation and reproducibility

This document defines the validation standard for the demographic forecasting project. It is a protocol, not a claim that the notebook has already passed every check.

## 1. Keep three timelines separate

- **Historical estimates:** observations/estimates published in the UN WPP 2024 data.
- **UN projections:** the UN's own projection series, which are scenario-based projections rather than observed future outcomes.
- **Model predictions:** outputs produced by Prophet or scikit-learn models trained in this project.

Do not describe a model as accurate merely because its future curve looks plausible or resembles the UN projection.

## 2. Use time-aware evaluation

Random train/test splits are inappropriate for forecasting because they can let future years influence training. Use a chronological holdout and, ideally, rolling-origin evaluation:

1. Choose an evaluation period before model fitting.
2. Fit every transformation and model using training years only.
3. Predict the same held-out years for every model.
4. Compare with a simple baseline, such as carrying forward the last observed value or a clearly specified trend baseline.
5. Report MAE and RMSE on the same target, units, and years. State the number of evaluation years.
6. Keep future projection years out of model selection unless explicitly treated as inputs in a clearly defined scenario exercise.

## 3. Prevent leakage

- Do not use features calculated from the target's future values.
- If scaling or imputation is needed, fit it on the training period only; use a scikit-learn Pipeline where practical.
- If forecasting multiple years ahead, future fertility, mortality, migration, or age-structure values may not be available at prediction time. State whether the task is a same-year explanatory estimate or a true multi-year-ahead forecast.
- When using derived age-group totals, validate that source age bands are exhaustive and non-overlapping.

## 4. Report metrics honestly

| Model | Training years | Test years | MAE | RMSE | Baseline beaten? |
|---|---|---|---:|---:|---|
| Baseline | To be filled from run | To be filled from run | — | — | — |
| Prophet | To be filled from run | To be filled from run | — | — | — |
| Random Forest | To be filled from run | To be filled from run | — | — | — |
| Random Forest + age structure | To be filled from run | To be filled from run | — | — | — |

Populate this table from actual notebook output. Do not invent metrics or assume a model wins before running the same evaluation protocol.

## 5. Define risk indices transparently

For each index, document input variables and units; directionality; normalization method and reference range; weights and rationale; missing-data handling; and whether thresholds have external validation.

If the composite score is an unweighted sum, say so and explain whether component scales are comparable. A composite index is a constructed analytical indicator, not a validated probability of a demographic crisis.

## 6. Reproducibility checklist

- Record Python version and direct package dependencies.
- Record random seeds for stochastic models.
- Document exact data files and source release.
- Ensure notebook cells run top-to-bottom from a clean environment.
- Save plots and metric tables from the same evaluation run.
- Do not publish restricted, confidential, or non-public internship material. Use only data and artifacts approved for public release.