# SUPPORT2 Mortality Prediction

Predicting in-hospital mortality from the SUPPORT2 dataset using classical ML and XGBoost.  
Target variable: binary survival outcome. Key stratifier: income bracket.

## Project Structure

project/
├── data/
│   ├── raw/                # Original SUPPORT2 dataset (untouched)
│   ├── processed/          # Cleaned and feature-engineered data
│   ├── models/             # Serialized model files (.pkl / .h5)
│   ├── outputs/            # CSVs: predictions, metrics, subgroup analyses
│   └── visualizations/     # Confusion matrices, PR curves, calibration plots
├── notebooks/
│   ├── 01_EDA.ipynb
│   ├── 02_Preprocessing.ipynb
│   ├── 03_Baseline_Model.ipynb
│   ├── 04_Advanced_Models.ipynb
│   ├── 05_Evaluation.ipynb
│   └── 06_Final_Model.ipynb
├── config.py               # Paths, hyperparameters, random seed
├── requirements.txt
└── README.md

## Quickstart

```bash
pip install -r requirements.txt
# Run notebooks in order: 01 → 06
```

## Key Results

| Income Group | Mortality Rate |
|---|---|
| under $11k | 67.2% |
| $11–$25k | 66.5% |
| $25–$50k | 65.9% |
| >$50k | 65.7% |

Mortality rates are relatively stable across income groups (~66%), but average charges
differ substantially — higher-income patients incur significantly higher costs.

## Models

Baseline: Logistic Regression, Decision Tree  
Advanced: Random Forest, Gradient Boosting, XGBoost  
Final model: XGBoost (see `data/XGBOOST/`)

## Dataset

[SUPPORT2](https://hbiostat.org/data/) — Study to Understand Prognoses and Preferences
for Outcomes and Risks of Treatments. ~9,000 hospitalized patients, 1989–1994.
