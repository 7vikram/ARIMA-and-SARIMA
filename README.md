
# **Sales Forecasting Project**

This repository contains time series forecasting projects for two datasets: **Champagner Sales** and **Super Store Sales**. It leverages ARIMA and SARIMA models for the Champagner dataset and ARIMA modeling for the Super Store dataset. The projects evaluate forecast accuracy using metrics like MAE and RMSE.

---

## **📄 Project Overview**

### **🎯 Objectives**
1. **Champagner Sales**  
   - Preprocess and forecast Champagner sales for the next 12 months using both ARIMA and SARIMA models.  
   - Compare the performance of ARIMA and SARIMA models based on accuracy metrics.  
2. **Super Store Sales**  
   - Forecast sales across three specific scenarios using ARIMA models:  
     - **Overall Sales**  
     - **South Region - Technology Category**  
     - **West Region - Office Supplies Category**  

---

## **🛠 Methodology**

### **Champagner Sales**
1. **Data Preprocessing**  
   - Converted sales data to a time series indexed by date.  
   - Performed stationarity tests using the Augmented Dickey-Fuller (ADF) test.  
   - Differenced the data if needed for stationarity.  

2. **Forecasting Models**  
   - **ARIMA Model**: Fitted and forecasted using ARIMA with optimal parameters.  
   - **SARIMA Model**: Used Seasonal ARIMA to account for seasonality.  

3. **Evaluation**  
   - Compared MAE and RMSE between ARIMA and SARIMA models.  

4. **Visualization**  
   - Plotted historical sales and forecasts for both models.

---

### **Super Store Sales**
1. **Data Preprocessing**  
   - Converted `Order Date` to datetime format and set it as the index.  
   - Sorted data chronologically and handled missing values.  

2. **Normalization and De-normalization**  
   - Applied `MinMaxScaler` to normalize sales data for each variation independently.  
   - De-normalized forecasts and actual values for interpretability.  

3. **Stationarity Check**  
   - Conducted the Augmented Dickey-Fuller (ADF) test.  
   - Applied differencing if data was non-stationary.  

4. **Forecasting with ARIMA**  
   - Modeled each variation using ARIMA, selecting parameters `(1,1,1)`.  
   - Generated 12-month forecasts for each variation.  

5. **Evaluation**  
   - Calculated **Mean Absolute Error (MAE)** and **Root Mean Squared Error (RMSE)** to evaluate forecast accuracy.  
   - Identified the variation with the lowest errors.

6. **Visualization**  
   - Historical sales trends and forecasts were plotted for each variation.

---

## **📊 Results**
### **Champagner Sales**  
- SARIMA outperformed ARIMA in capturing seasonality for the Champagner dataset.  
- Visualizations compared the performance of ARIMA and SARIMA models.  

### **Super Store Sales**  
- Accuracy Metrics (MAE and RMSE) were computed for each variation:  
   - **Overall Sales**  
   - **South Region - Technology Category**  
   - **West Region - Office Supplies Category**  

- **Best-Performing Variation:**  
   - Based on MAE and RMSE, the variation with the lowest error is highlighted in the script output.

---

## **🔮 Future Enhancements**

### Recommendations for Advanced Forecasting:
1. **Prophet (by Facebook):** Excellent for capturing seasonality and trends in the presence of holidays and external events.  
2. **LSTM Neural Networks:** Effective for learning non-linear patterns in sequential data.  
3. **Ensemble Models:** Combining ARIMA and machine learning models like XGBoost for hybrid forecasting.  

---

## **🚀 Usage**
1. Clone this repository and ensure the datasets (`champagner.csv` and `super_store.csv`) are in the same directory as the scripts.  
2. Run the respective Python scripts (`champagner_forecasting.ipynb` and `super_store_forecasting.ipynb`) using Jupyter Notebook or any Python IDE.  
3. Results, including metrics and visualizations, will be generated for both datasets.

---

## **📦 Dependencies**
- Python 3.x  
- pandas  
- numpy  
- matplotlib  
- statsmodels  
- scikit-learn  

Install dependencies using:  
```bash
pip install pandas numpy matplotlib statsmodels scikit-learn
```

---

## **📬 Contact**
For questions or further improvements, please reach out to:  
**Vikram Purohit**  
**purohitvikram77@gmail.com**  
