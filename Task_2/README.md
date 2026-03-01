# Stock Price Prediction (Short-Term)

## Task Objective
The goal of this task is to predict the **next day's closing price** of a stock using historical stock market data. This helps analyze short-term trends and evaluate the performance of different regression models for stock price prediction.

---

## Dataset
- **Source:** Historical stock data fetched using the **yfinance** Python library.
- **Features Used:** `Open`, `High`, `Low`, `Volume`.
- **Target Variable:** Next day's `Close` price.
- **Example Stock:** Apple Inc. (`AAPL`).
- **Date Range:** January 1, 2020 – January 31, 2026.

---

## Step-by-Step Procedure

### 1. Data Loading
- Used the `yfinance` library to download historical stock data.
- Displayed the first few rows to inspect the dataset structure.
- Checked dataset shape, column names, and missing values.

### 2. Data Preprocessing
- Selected relevant features: `Open`, `High`, `Low`, `Volume`.
- Set the target variable as the **next day's Close price** using `shift(-1)`.
- Removed the last row (since its target would be `NaN`).

### 3. Train-Test Split
- Split data into training (80%) and testing (20%) sets.
- Used **time series split** (no shuffling) to preserve chronological order.

### 4. Model Training
Two regression models were applied:

1. **Linear Regression**
   - Captures linear relationships between features and the target.
   - Trained on historical data.

2. **Random Forest Regressor**
   - Captures non-linear patterns in the data.
   - Used 100 estimators and trained on the same dataset.

### 5. Model Evaluation
- Evaluated models using:
  - **RMSE (Root Mean Squared Error)**
  - **R² Score**
- Results:

| Model                 | RMSE   | R² Score |
|-----------------------|--------|----------|
| Linear Regression     | 4.32   | 0.97     |
| Random Forest         | 19.28  | 0.42     |

**Observations:**
- Linear Regression performed exceptionally well for short-term prediction.
- Random Forest underperformed, likely due to the small number of features and linear trends dominating the data.

### 6. Visualization
- Plotted **actual vs predicted closing prices** for both models.
- Linear Regression closely followed the actual price trend.
- Random Forest predictions deviated significantly.

### 7. Insights
- Short-term stock prices can be effectively predicted using simple linear models with basic market features.
- Random Forest may require additional features or hyperparameter tuning to improve performance.
- For more advanced predictions, features like moving averages, RSI, MACD, or LSTM/GRU models can be incorporated.

**Key Takeaways: **
- Both Linear Regression and Random Forest were applied.
- Linear Regression was highly accurate for next-day predictions (R² = 0.97).
- Visualizations provide a clear comparison of model predictions versus actual prices.
- Demonstrates basic time-series regression, feature selection, model training, and evaluation workflows.
