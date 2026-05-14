# Regression Analysis

A short data science exercise that builds a **Linear Regression model** to predict
restaurant tip amounts using the classic *tips* dataset.

## Dataset

[tips.csv](https://raw.githubusercontent.com/mwaskom/seaborn-data/master/tips.csv)
244 rows of restaurant tipping data with features:
total_bill, tip, sex, smoker, day, time, size.

## How to Run

1. Open [Google Colab](https://colab.research.google.com)
2. Click **File → Upload notebook** and upload `tips_regression.ipynb`
3. Click **Runtime → Run all**
4. The chart will download automatically as `feature_coefficients.png`

No installations needed — all libraries are pre-installed in Colab.

## Results Summary

| Metric | Value | Interpretation                                 |
|--------|-------|------------------------------------------------|
| RMSE   | 0.83  | Predictions are off by ~$0,83 on average       |
| R²     | 0.44  | ~44% of tip variance is explained by the model |

**Most influential variable:** size — party size has the highest absolute
coefficient (0.2403), meaning larger groups are the strongest predictor of
higher tips. See `Notes.md` for the full explanation.

## Files

| File                      | Description                        |
|---------------------------|------------------------------------|
| `tips_regression.ipynb`   | Full analysis notebook             |
| `Notes.md`                | Findings and variable explanation  |
| `feature_coefficients.png`| Bar chart of feature coefficients  |
| `README.md`               | This file                          |
