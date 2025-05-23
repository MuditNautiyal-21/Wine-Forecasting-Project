# 🍷 Wine Sales Forecasting – Rose & Sparkling

## 🧠 Overview
This project forecasts monthly sales for **two wine categories** — *Rose* and *Sparkling* — using various time series models. The objective is to assist **ABC Estate Wines** with accurate demand forecasting for inventory planning and marketing strategy.

---

## 📊 Dataset Summary

- **Source**: ABC Estate Wines (academic dataset)
- **Period**: 1980 to 1995 (monthly data)
- **Targets**: Sales volume for Rose and Sparkling wine
- **Features**: Univariate time series (no regressors)

---

## 🎯 Objectives

- Forecast next 12 months of sales for both wine types
- Compare forecasting models and select best performers
- Evaluate using Root Mean Squared Error (RMSE)
- Translate findings into business-relevant recommendations

---

## 🧪 Models Evaluated

| Model                     | Description                               |
|---------------------------|-------------------------------------------|
| Naïve Forecast             | Uses last known value                     |
| Simple Average             | Mean value for all prior months           |
| Moving Average             | Smoothed average of recent `n` periods    |
| Linear Regression          | Trend-based model                         |
| Exponential Smoothing      | Includes Holt-Winters seasonal modeling   |
| ARIMA (Auto & Manual)      | Autoregression with differencing          |
| SARIMA (Auto & Manual)     | Seasonal ARIMA for cyclic patterns        |

---

## 📈 Model Performance (RMSE)

| Wine Type   | Best Model                   | RMSE    |
|-------------|------------------------------|---------|
| **Rose**    | Triple Exponential Smoothing | **9.64**   |
|             | SARIMA (Manual)              | 27.25   |
|             | ARIMA (Auto)                 | 37.64   |
|             | Naïve                        | 39.23   |
|             | Linear Regression            | 103.88  |
| **Sparkling**| Triple Exponential Smoothing | **336.71** |
|             | SARIMA (Auto)                | 855.44  |
|             | ARIMA (Manual)               | 1308.12 |

---

## 📊 Visual Forecasts

![Rose Forecast](./images/rose_forecast.png)
![Sparkling Forecast](./images/sparkling_forecast.png)

> Forecast graphs created using Holt-Winters and SARIMA methods.

---

## 💡 Business Insights

- **Rose Wine** shows strong seasonality with stable demand, ideal for traditional smoothing.
- **Sparkling Wine** has higher volatility but benefits from smoothing-based methods.
- ARIMA and SARIMA models underperform due to limited explanatory features.
- Best model across both categories: **Triple Exponential Smoothing (Holt-Winters)**

---

## 📂 Folder Structure

Wine-Forecasting-Project/
├── Rose/
│ ├── PROJECT_TSF_Rose_DATA_MODEL.ipynb
│ └── Rose TSF PROJECT.pdf
├── Sparkling/
│ ├── PROJECT_TSF_Sparkling_DATA_MODEL.ipynb
│ └── Sparkling TSF PROJECT.pdf
├── images/
│ ├── rose_forecast.png
│ └── sparkling_forecast.png
├── README.md
└── requirements.txt
