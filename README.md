# **Time Series Forecasting in Python**

## **1. Project Overview**

This project presents a **Time Series Forecasting model** built in Python to predict weekly demand for bakery products.
It demonstrates how statistical forecasting techniques can be used to support **data-driven demand planning**, **inventory optimization**, and **sales forecasting** in retail and food businesses.

The notebook includes **data preparation**, **multiple forecasting models**, **model evaluation**, and **performance visualization**. It provides a full workflow from raw data to actionable insights.

---

## **2. Key Business Questions**

The project answers:

* What is the expected sales demand for key bakery products in the upcoming week?
* Which forecasting method provides the most accurate predictions?
* How do baseline models compare to automated ARIMA models?
* How can forecasting insights improve production and inventory decisions?

---

## **3. Python Features**

### **Data Preparation**

* **Dataset:** Daily bakery sales dataset has product-level transaction data.
* **Cleaning:** Removed incomplete time series and irrelevant columns.
* **Aggregation:** Grouped and filtered to retain products with at least 4 weeks of history.

---

### **Forecasting Models**

Built using the [**StatsForecast**](https://github.com/Nixtla/statsforecast) library:

* **Naive Model** – uses the last observed value as the forecast.
* **Historic Average** – averages past sales to predict future demand.
* **Window Average (7-day)** – calculates moving averages to smooth fluctuations.
* **Seasonal Naive (weekly seasonality)** – repeats past weekly patterns.
* **AutoARIMA** – automatically selects the best ARIMA and SARIMA model for each product.

---

### **Evaluation**

* **Metric:** Mean Absolute Error (MAE)
* Compared model performance across all products.
* Visualized MAE scores for clear comparison of forecast accuracy.

---

### **Visualization**

* **Time Series Plots** for actual vs. predicted demand.
* **Bar Chart of MAE Scores** to identify top-performing models.
* Used `matplotlib` and `utilsforecast.plotting` for clear, business-friendly visuals.

---

## **4. Insights**

### **Model Performance Comparison**

Three forecasting models were evaluated to identify the most accurate approach for predicting weekly bakery demand.
The comparison below is based on **Mean Absolute Error (MAE)**. Lower values means better accuracy.

| Metric  | Seasonal Naive | ARIMA |   SARIMA  |
| :------ | :------------: | :---: | :-------: |
| **MAE** |      21.12     | 21.17 | **19.28** |

---

### **Key Findings**

* The **SARIMA model has the lowest MAE (19.28)**, outperforms both Seasonal Naive and ARIMA.
  It’s the most reliable model for forecasting product demand in this bakery context.
* **Seasonal Naive (21.12 MAE)** performes well given its simplicity. It serves as a strong baseline. It's fast, interpretable, and suitable for quick operational forecasts.
* **ARIMA (21.17 MAE)** provides quite similar accuracy to Seasonal Naive but requires more computation.
* The improvement from **SARIMA** demonstrates the value of modeling both **seasonal and non-seasonal patterns**, essential in retail environments with strong weekly cycles.

---

### **Business Impact**

* Enables bakery managers to **anticipate weekly demand** more accurately.
* Supports **inventory and staffing decisions** by reducing waste and stockouts.
* Demonstrates **scalable forecasting methods** adaptable to other retail datasets.

---

## **5. Project Structure**

```
README.md                      : Main project documentation  
Time_Series_Forecasting.ipynb  : Python notebook with full workflow  
```

---

## **6. How to Use**

### **Option 1: Run in Jupyter Notebook**

1. Open `Time_Series_Forecasting.ipynb` in Jupyter or VS Code.
2. Run all cells to reproduce results and visualizations.

### **Option 2: View in GitHub**

* Click the notebook file to preview code and charts directly.

---

