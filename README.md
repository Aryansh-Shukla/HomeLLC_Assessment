# 📈 Forecasting the Home Price Index Using Economic Indicators (2005–2025)

This project analyzes and models the **U.S. Home Price Index (HPI)** from 2005 to 2025 using key macroeconomic indicators. The goal is to understand how different economic factors influence home prices over time and accurately predict HPI values.

---

## 📊 Objective

To **study the impact and influence of economic indicators** like GDP, CPI, unemployment rate, population growth, and interest rates on the national Home Price Index and develop a predictive model.

---

## 🗂️ Dataset

The data was sourced from **Kaggle**:  
🔗 [Factors Affecting USA National Home Prices](https://www.kaggle.com/datasets/madhurpant/factors-affecting-usa-national-home-prices)

Time range: **January 2005 – January 2025**  
Frequency: **Monthly**  
Files used from the dataset include:
- `Home-Price-Index.csv`
- `GDP.csv`
- `consumer-price-index.csv`
- `unemployment-rate.csv`
- `Mortgage.csv`
- `population-growth.csv`
- `FedFunds.csv`

---

## 🛠️ Tools & Libraries

- Python, Pandas, NumPy
- Scikit-learn (Linear Regression, Ridge)
- Matplotlib & Seaborn (Visualizations)
- Jupyter Notebook

---

## 🔍 Exploratory Data Analysis (EDA)

- Time-series line plots of all features vs time
- Correlation heatmap with HPI
- Variance Inflation Factor (VIF) to detect multicollinearity
- Feature distribution analysis
- Lagging `HPI` by 1 month to capture temporal dependency (`HPI_lag1`)

---

## 🧠 Modeling Approach

### ✅ Final Model: **Ridge Regression with Lag Feature**

- **Features Used**: `GDP`, `CPI`, `Unemployment Rate`, `Population Growth`, `HPI_lag1`
- **Train-Test Split**: 80% train / 20% test (chronological split)
- **Evaluation Metrics**:
  - R² Score: `0.997`
  - RMSE: `1.69`

### 🔁 Lag Feature Justification
Lagging HPI (using previous month’s value) helps the model capture historical momentum in housing prices.

---

## 📈 Results

### 📉 Actual vs Predicted Plot

A line plot comparing actual HPI and predicted HPI shows near-perfect overlap, confirming the model’s high accuracy.

### 🧾 Feature Coefficients

| Feature             | Influence on HPI |
|---------------------|------------------|
| HPI_lag1            | Very Strong +ve  |
| GDP                 | Strong +ve       |
| CPI                 | Moderate +ve     |
| Unemployment Rate   | Negative          |
| Population Growth   | Negative          |

---

## 📌 Key Insights

- **HPI is strongly autocorrelated**: Past values heavily influence current prices.
- **GDP and CPI drive price increases**.
- **Unemployment and population growth** act as suppressors on price movement.
- Ridge regression effectively handled multicollinearity between economic variables.

---

## 🧠 Future Improvements

- Incorporate additional lags (2 or 3 months).
- Try time-series-specific models (e.g., ARIMAX, LSTM).
- Add external shocks (e.g., COVID impact markers).
- Visualize feature importance dynamically over time.

---

## ✅ Conclusion

This project successfully models the **Home Price Index** using a mix of economic indicators and a lagged feature, achieving **97.7% accuracy**. It provides valuable insights into the economic drivers of housing prices in the U.S. over two decades.

---
