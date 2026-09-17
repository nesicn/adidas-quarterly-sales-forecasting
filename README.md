# Adidas Quarterly Sales Time Series Analysis & Forecasting
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1yaW0RouOt45UphljCRckgFi4TI29lE13?usp=sharing)
[![Python 3.8+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/downloads/)

An end-to-end statistical time series analysis and forecasting project built on Adidas quarterly revenue data spanning from 2000 to 2021. The project leverages STL decomposition to analyze trend and seasonality, Augmented Dickey-Fuller (ADF) testing for stationarity, and SARIMAX modeling for revenue forecasting.

---

## 📌 Project Overview
Revenue forecasting plays a critical role in strategic financial planning and inventory management. This project analyzes 88 quarterly financial reports from Adidas to uncover long-term growth trends, identify seasonal sales peaks, and build predictive statistical models.

## 📊 Dataset
* **Source:** Adidas Quarterly Sales Dataset (`adidas-quarterly-sales.csv`)
* **Time Span:** 2000 Q1 – 2021 Q4 (88 observations)
* **Features:**
  * `Time Period`: Quarterly timestamp format (e.g., `2000Q1`)
  * `Revenue`: Quarterly sales revenue figures

## 🛠 Methodology & Analytical Pipeline
1. **Data Preprocessing:** Converted quarterly string representations into proper time-indexed datetime objects using `pd.PeriodIndex`.
2. **Exploratory Data Analysis (EDA):** Visualized revenue trajectory across two decades to identify structural changes and seasonal variations.
3. **Stationarity Testing:** Applied the **Augmented Dickey-Fuller (ADF)** test (`adfuller`) to verify whether the series exhibits non-stationary properties.
4. **Time Series Decomposition:** Used **STL Decomposition** to isolate the core components:
   * **Trend:** Overall directional movement of sales.
   * **Seasonality:** Repeating quarterly fluctuations.
   * **Residuals:** Random noise and unmodeled variance.
5. **Predictive Modeling:** Configured a **SARIMAX** model to capture both seasonal patterns and exogenous/auto-regressive factors.

## 💻 Tech Stack
* **Language:** Python 3.x
* **Data Handling:** Pandas, NumPy
* **Time Series Analysis:** Statsmodels (`SARIMAX`, `STL`, `adfuller`)
* **Data Visualization:** Matplotlib, Seaborn

## 🚀 Getting Started

### Prerequisites
Ensure Python 3.8+ is installed on your environment.

### Installation
Clone the repository:
   ```
   git clone https://github.com/nesicn/adidas-quarterly-sales-forecasting.git
   cd adidas-quarterly-sales-forecasting
   ```
Install Dependencies:

```
pip install -r requirements.txt
```
Run Notebook / Script:
```
code .
```

Open ```notebooks/adidas-time-series-analysis.ipynb``` in Visual Studio Code or Google Colab.
