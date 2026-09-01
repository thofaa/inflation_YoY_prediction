# Inflation YoY Prediction

Multiple linear regression to predict Indonesian Inflation YoY using **BI Rate**, **M2** (normalized), and current **Inflation** as predictors.

## Data

| File | Description |
|------|-------------|
| `data/BI_Rate_2017_2026.json` | BI Rate decisions |
| `data/M2M1_Norm_2017_2026.json` | M1 / M2 with min-max normalized M2 |
| `data/Inflation_YoY_2017_2026.json` | Inflation YoY per period |

## Notebooks

- `Linear_Regression_Model_Nplus1.ipynb` — predicts Inflation at period **n+1** from period-n predictors

## Mathematical Models

**Model N+1 (next period prediction, includes autoregressive current inflation):**

$$Inflasi_{(n+1)} = 0.5410 - 0.0838 \cdot BIRate_{(n)} + 0.0734 \cdot M2_{(n)} + 0.9420 \cdot Inflasi_{(n)}$$

R² = 0.8739
