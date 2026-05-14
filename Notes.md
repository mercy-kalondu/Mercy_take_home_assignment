# Model Findings

### Most Influential Variable: `size`
Of all six features fed into the linear regression model
(total_bill, size, sex, smoker, day, time),
size has the largest absolute coefficient (0.2403), followed by smoker(-0.1917) and total_bill (0.0940).

### Feature Coefficients (from model output)

| Feature    | Coefficient |
|------------|-------------|
| size       |  0.2403     |
| smoker     | -0.1917     |
| total_bill |  0.0940     |
| time       |  0.0612     |
| sex        |  0.0327     |
| day        | -0.0068     |

### Why size makes sense as the top predictor

- **More diners = higher tip:** Larger party sizes naturally lead to bigger bills and, in turn, larger absolute tip amounts.
- **Social dynamics:** Larger groups may feel more social pressure to leave a visible tip.
- **Note on `smoker`:** Its negative coefficient (-0.1917) suggests that smokers in this dataset tended to tip slightly less on average.
- **`total_bill` still matters:** Although it ranks third, bill size and party size are naturally correlated, that is they contain larger groups spend more.

## Model Performance

| Metric | Value | Interpretation                                  |
|--------|-------|-------------------------------------------------|
| RMSE   | 0.83 | Predictions are off by ~$0.83 on average        |
| R²     | 0.44 | ~44% of tip variance is explained by the model  |

## Visualisation

feature_coefficients.png — a horizontal bar chart showing each feature's
regression coefficient. Size is the dominant positive predictor, with
smoker  being the strongest negative predictor.

## Potential Next Steps

- Engineer a tip_rate feature (tip / total_bill) to explore percentage-based patterns.
- Try a **Random Forest** or **Gradient Boosting** regressor for a non-linear fit.
- Add cross-validation to get more stable RMSE / R² estimates.
