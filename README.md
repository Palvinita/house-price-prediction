# California House Price Prediction

Linear regression built from scratch (NumPy, gradient descent) on the
California Housing dataset (Kaggle: camnugent/california-housing-prices).

## What I did
- Explored the data: 207 missing total_bedrooms, 965 rows capped at 500001
- 80/20 train/test split, filled missing values with the train median
- Standardized features using train mean and std
- Implemented cost, gradient and gradient descent without ML libraries

## Results (one feature: median_income)

| Metric | Value |
|---|---|
| Test RMSE | $84,914 |
| Test R² | 0.464 |
| Baseline RMSE (always predict the mean) | $116,017 |

The model beats the baseline, but one feature explains less than half of
the price variation. Location, age and size also matter.

## Next
- Add more features (multiple weights)
- Vectorize gradient descent with NumPy
- Compare results with and without the 965 capped rows