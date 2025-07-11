# 📈 Stock Price Prediction using LSTM

---

## 🚀 Project Overview

This project implements a deep learning model using **Long Short-Term Memory (LSTM)** networks to predict future stock prices based on historical closing price data.

It includes:
- ✅ Real-time financial data via `yfinance`
- 🧠 A multi-layered LSTM architecture
- 🔮 Next **7-day price forecasting**
- 📊 Rich visualizations including actual vs predicted, error plots, and interactive Plotly graphs

---

---

## 📦 Technologies Used

- Python 3.10+
- TensorFlow / Keras
- NumPy & Pandas
- Matplotlib & Seaborn
- Plotly (for interactive charts)
- yfinance (for stock data)

---

## 🧠 LSTM Model Summary

```python
model = Sequential()

model.add(Bidirectional(LSTM(units=100, return_sequences=True), input_shape=(X.shape[1], 1)))
model.add(Dropout(0.3))

model.add(LSTM(units=120, return_sequences=True))
model.add(Dropout(0.3))

model.add(LSTM(units=100, return_sequences=True))
model.add(Dropout(0.3))

model.add(LSTM(units=80, return_sequences=False))
model.add(Dropout(0.3))

model.add(Dense(units=64, activation='relu'))
model.add(Dropout(0.2))

model.add(Dense(units=1))

