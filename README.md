
# **Super Store Sales Forecasting Project**

This repository contains a time series forecasting project for sales data from a Super Store dataset. The project leverages ARIMA modeling to forecast sales across three specific variations and evaluates their accuracy using metrics like MAE and RMSE.

---

## **📄 Project Overview**

### **🎯 Objective**
The primary goal is to preprocess, normalize, and forecast sales data for the following scenarios:
1. **Overall Sales** - Forecasting total sales for all regions and categories.
2. **South Region - Technology Category** - Forecasting sales specific to the "Home Office" segment within the "South" region for the "Technology" category.
3. **West Region - Office Supplies Category** - Forecasting sales specific to the "Consumer" segment within the "West" region for the "Office Supplies" category.

### **🛠 Methodology**
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

---

## **📊 Results**
- **Accuracy Metrics:**  
   - Overall Sales  
   - South - Technology  
   - West - Office Supplies  

- **Best-Performing Variation:**  
   - Based on MAE and RMSE, the variation with the lowest error is highlighted in the script output.

---

## **📈 Visualizations**
- Historical sales trends and forecasts are plotted for each variation using Matplotlib for clear interpretability.

---

## **🔮 Future Enhancements**

### Recommendations for Advanced Forecasting:
1. **Prophet (by Facebook):** Excellent for capturing seasonality and trends in the presence of holidays and external events.  
2. **LSTM Neural Networks:** Effective for learning non-linear patterns in sequential data.  
3. **Ensemble Models:** Combining ARIMA and machine learning models like XGBoost for hybrid forecasting.  

---

## **🚀 Usage**
1. Clone this repository and ensure the dataset (`super_store.csv`) is in the same directory as the script.  
2. Run the Python script using Jupyter Notebook or any Python IDE.  
3. Results, including metrics and visualizations, will be generated for all three variations.

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
