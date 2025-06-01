# 📈 Stacked Ensembling & Algorithmic Trading Strategy (FTSE 100)

This project implements multiple machine learning models and a stacked ensemble to forecast weekly returns of the FTSE 100 index. Predicted returns are used to design and backtest two systematic trading strategies: **Long/Short** and **Proportional Investing**. We evaluate model and trading performance using key financial metrics like **Sharpe Ratio**, **Treynor Ratio**, and **Directional Accuracy**.

---

## 🧠 Project Objective

- Forecast **weekly log returns** for the FTSE 100 index using financial indicators.
- Apply model predictions to rule-based trading strategies.
- Compare model and strategy performance using industry-standard metrics.

---

## 🗂️ Repository Contents

- 📄 `Stacked_Ensembling_Algo_report.pdf` – Full academic report detailing methods, results, and evaluation.
- 📒 `Stacked Ensembling & Algorithmic Trading Strategy (FTSE 100).ipynb` – Jupyter notebook with code for feature engineering, model building, and trading strategy simulation.

---

## 📊 Data Description

- **Source**: Yahoo Finance – FTSE 100 index
- **Frequency**: Weekly
- **Date Range**: 18 April 2009 – recent
- **Target**: Cumulative weekly log returns
- **Features**:
  - EMA(5), EMA(20)
  - MACD
  - RSI
  - Volume
  - Lagged returns

---

## ⚙️ Models Used

We trained the following base learners:

- ✅ Ridge Regression  
- ✅ Logistic Regression  
- ✅ XGBoost  
- ✅ Random Forest *(🧠 implemented by me)*  
- ✅ Support Vector Machine (SVM) *(🧠 implemented by me)*

These were combined into a **stacked neural network ensemble** *(🧠 built by me)* to improve predictive accuracy and consistency.

---

## 💸 Trading Strategies

Two trading strategies were designed using the model predictions:

### 1️⃣ Long/Short Strategy
- Go **long** if predicted return is positive
- Go **short** if predicted return is negative
- Evaluate cumulative return and Sharpe Ratio

### 2️⃣ Proportional Strategy
- Allocate capital **proportionally** to the strength of the predicted return
- Adjust position size based on forecast confidence

---

## 📈 Key Performance Metrics

| Model               | In-Sample Sharpe | Out-of-Sample Sharpe | Directional Accuracy |
|--------------------|------------------|-----------------------|------------------------|
| Ridge Regression    | 0.728            | 0.729                 | **89.33%**             |
| Logistic Regression | 2.486            | 1.402                 | —                      |
| XGBoost             | 0.501            | 0.227                 | **51.33%**             |
| Random Forest       | 0.730            | 0.216                 | —                      |
| SVM                 | 3.222            | 0.241                 | —                      |
| **Neural Ensemble** | 0.235            | 0.295                 | —                      |

---

## 👨‍💻 My Contributions (Pranjal Kharbanda)

I contributed to the **design, modeling, and evaluation** of all three portfolio models. My specific responsibilities included:

### ✅ Random Forest
- Built and tuned the model using scikit-learn
- Performed out-of-sample evaluation and feature analysis

### ✅ SVM (Support Vector Machine)
- Implemented kernel-based return classification
- Tuned hyperparameters using cross-validation
- Evaluated directional signals

### ✅ Neural Network Ensemble
- Constructed and trained stacked ensemble using neural networks
- Integrated base model predictions into final forecast
- Tested ensemble performance on trading strategies

---

## 🧠 What I Learned

- How to apply **machine learning models to financial time series**
- The power and limitations of **stacked ensembling** in trading
- Importance of using **Sharpe**, **Treynor**, and **Directional Accuracy** as evaluation tools
- Practical understanding of **algorithmic strategy design** and **backtesting**

---

## 🚀 Future Enhancements

- Integrate macroeconomic variables and sentiment indicators
- Incorporate **rolling window re-training** and **walk-forward analysis**
- Evaluate **transaction costs** and **slippage** in trading simulation
- Extend ensemble to include deep learning models (e.g., LSTM)

---

> 📌 *This project was completed as part of the MSc Quantitative Finance curriculum at UCD Smurfit Business School. It blends financial modeling, machine learning, and trading strategy design in a real-world market context.*

---
