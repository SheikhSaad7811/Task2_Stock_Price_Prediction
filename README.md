# Task 2: Predict Future Stock Prices (Short-Term)

## 📌 Objective
The objective of this task is to **use historical stock data to predict the next day's closing price**.  
We apply regression models to stock market time series data fetched from the Yahoo Finance API using the `yfinance` Python library.

---

## 📊 Dataset Used
- **Source:** Yahoo Finance API (via `yfinance` library)  
- **Stock Example:** Apple Inc. (`AAPL`)  
- **Period:** January 2023 – December 2024  
- **Features Used:**
  - Open
  - High
  - Low
  - Volume
- **Target:** Next day's Close price

---

## 🛠 Models / Methods Applied
1. **Data Collection**
   - Retrieved using `yfinance.download()`
2. **Feature Engineering**
   - Created target column by shifting the Close price by 1 day
3. **Modeling**
   - Linear Regression *(optional)*
   - Random Forest Regressor *(default in example)*
4. **Evaluation**
   - **Mean Squared Error (MSE)**
   - **R² Score** (coefficient of determination)
5. **Visualization**
   - Line plot comparing actual vs predicted closing prices

---

## 📈 Key Results & Findings
- **Random Forest** performed better than simple Linear Regression in capturing non-linear stock price movements.
- Actual vs Predicted plot shows the model follows trends but may miss sudden spikes.
- R² Score typically between **0.85–0.95** for short-term predictions with sufficient historical data.

---

## 📦 Requirements
```bash
pip install pandas yfinance scikit-learn matplotlib
