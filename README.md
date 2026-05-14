# Regression Analysis
A short data science exercise that builds a **Linear Regression model** to predict restaurant tip amounts using the classic *tips* dataset. The goal is to identify which factors most influence how much a customer tips at a restaurant.
## Project Overview

This project uses the well-known `tips` dataset to explore tipping behaviour. We load and inspect the data, encode categorical variables, train a Linear Regression model, evaluate its performance, and visualise the most influential
features using a bar chart.
## Dataset

**Source:** [tips.csv](https://raw.githubusercontent.com/mwaskom/seaborn-data/master/tips.csv)

- 244 rows of restaurant tipping data
- 7 features: `total_bill`, `tip`, `sex`, `smoker`, `day`, `time`, `size`

| Column       | Type        | Description                          |
|--------------|-------------|--------------------------------------|
| total_bill   | Numeric     | Total bill amount in USD             |
| tip          | Numeric     | Tip amount in USD (target variable)  |
| sex          | Categorical | Gender of the bill payer             |
| smoker       | Categorical | Whether the party included a smoker  |
| day          | Categorical | Day of the week                      |
| time         | Categorical | Lunch or Dinner                      |
| size         | Numeric     | Number of people in the party        |


## Results Summary

| Metric | Value | Interpretation                                  |
|--------|-------|-------------------------------------------------|
| RMSE   | 0.83  | Predictions are off by ~$0.83 on average        |
| R²     | 0.44  | ~44% of tip variance is explained by the model  |

**Most influential variable:** size — party size has the highest absolute coefficient (0.2403), meaning larger groups are the strongest predictor of higher tips. See `Notes.md` for the full explanation.

## Visualisation

The bar chart below each feature's regression coefficient — how strongly and in which direction each variable influences the predicted tip.


