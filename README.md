# 📊 Stacked Ensembling & Algorithmic Trading Strategy (FTSE 100)

This project explores the application of ensemble machine learning models to forecast weekly returns of the **FTSE 100 Index**, with the objective of building algorithmic trading strategies. It was conducted as part of a group coursework at UCD Smurfit Business School.

The strategy uses a **neural network-based stacked ensemble** to combine the strengths of base learners like XGBoost, Ridge Regression, SVM, and Random Forest. We then used the model predictions to simulate various trading strategies and assess their performance.

---

## 🧠 Project Goal

- Forecast weekly **log returns** of the FTSE 100 Index using financial indicators and ML models.
- Use return predictions to implement:
  - **Long/Short trading strategy**
  - **Proportional investing strategy**
- Evaluate model and trading performance using Sharpe Ratio, Treynor Ratio, and Directional Accuracy.

---

## 📁 Project Files

- [`Stacked_Ensembling_Algo_report.pdf`](./Stacked_Ensembling_Algo_report.pdf): Final report detailing methodology, models, trading simulation, and results.
- [`Stacked Ensembling & Algorithmic Trading Strategy (FTSE 100).ipynb`](./Stacked%20Ensembling%20%26%20Algorithmic%20Trading%20Strategy%20%28FTSE%20100%29.ipynb): Jupyter notebook with full Python code for data cleaning, modeling, and performance evaluation.

---

## 📈 Data Description

- **Source**: FTSE 100 weekly OHLCV data from Yahoo Finance
- **Period Covered**: 18 April 2009 – End of dataset
- **Frequency**: Weekly
- **Target Variable**: Cumulative weekly **log returns**
- **Features Engineered**:
  - Exponential Moving Averages: EMA5, EMA20
  - MACD (Moving Average Convergence Divergence)
  - RSI (Relative Strength Index)
  - Volume-based indicators
  - Lagged Returns and Ratios

---

## 🤖 Models Used

| Model                  | Description                                     |
|------------------------|-------------------------------------------------|
| Ridge Regression       | Regularized linear regression                   |
| Logistic Regression    | Classification based on return sign            |
| XGBoost                | Gradient boosting framework                     |
| Random Forest          | Bagging-based decision tree ensemble            |
| SVM                    | Kernel-based classification                     |
| **Neural Ensemble**    | Final model combining base learners             |

---

## ⚙️ Trading Strategies Simulated

1. **Long/Short Strategy**:
   - Go long (buy) when return is predicted to be positive.
   - Go short (sell) when return is predicted to be negative.
   - Returns calculated as difference between actual return and cost of position.

2. **Proportional Strategy**:
   - Investment magnitude scaled based on predicted return.
   - Objective: capture higher profits during high-confidence predictions.

---

## 📊 Key Performance Metrics

| Model               | In-Sample Sharpe | Out-of-Sample Sharpe | Directional Accuracy |
|---------------------|------------------|-----------------------|------------------------|
| Ridge Regression    | 0.728            | 0.729                 | 89.33%                 |
| Logistic Regression | 2.486            | 1.402                 | —                      |
| XGBoost             | 0.501            | 0.227                 | 51.33%                 |
| Random Forest       | 0.730            | 0.216                 | —                      |
| SVM                 | 3.222            | 0.241                 | —                      |
| **Neural Ensemble** | 0.235            | 0.295                 | —                      |

---

## 👨‍💻 My Contributions

I took full responsibility for the following components:

- **Random Forest Model**:
  - Hyperparameter tuning and grid search
  - Cross-validation and out-of-sample testing
  - Analyzing feature importance

- **Support Vector Machine (SVM)**:
  - Kernel selection and performance comparison
  - Return prediction and classification threshold calibration

- **Neural Network Ensemble**:
  - Stacking model architecture and coding
  - Integration of base model predictions
  - Performance analysis of final ensemble vs individual models

---

## 💡 Key Learnings

- Applied ensemble learning (bagging, boosting, stacking) to financial time series
- Engineered predictive indicators for return forecasting
- Simulated realistic algorithmic trading strategies in Python
- Evaluated financial model performance with Sharpe and Treynor Ratios
- Gained practical experience with tools like `scikit-learn`, `XGBoost`, `Keras`, and `pandas`

---

## 🚀 Future Improvements

- Include macroeconomic factors (interest rates, inflation)
- Try LSTM or GRU-based deep learning for sequential data
- Apply transaction costs and slippage to simulate real-world conditions
- Test generalization on other indices (e.g. S&P 500, DAX)

---

> 📌 *This project represents a blend of data science and quantitative finance, and showcases my ability to build and evaluate predictive models in high-stakes decision-making environments.*
