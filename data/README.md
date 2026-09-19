# Adidas Quarterly Sales Dataset

## Overview & Source

This folder documents the dataset used in the quarterly revenue time series analysis and forecasting project. The dataset contains 22 years of continuous quarterly financial reports for Adidas.

* **Dataset File:** `adidas-quarterly-sales.csv`
* **Format:** CSV
* **Size:** 88 records, 2 columns
* **Time Span:** 2000 Q1 – 2021 Q4

## Data Dictionary

| Feature | Data Type | Description |
| :--- | :--- | :--- |
| `Time Period` | String | Quarterly timestamp identifier (e.g., `2000Q1`, `2021Q4`) |
| **`Revenue`** | **Float / Target** | **Quarterly net sales revenue figure** |

---

## Accessing the Data

To load the dataset and convert the timestamp into a proper time-indexed pandas dataframe:

```python
import pandas as pd

# Load dataset
df = pd.read_csv('data/adidas-quarterly-sales.csv')

# Convert quarterly string representation into Pandas PeriodIndex
df['Time Period'] = pd.PeriodIndex(df['Time Period'], freq='Q')
df.set_index('Time Period', inplace=True)
