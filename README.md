# NRM Vegetation Cover Early Warning System (EWS) Pipeline

This Jupyter Notebook provides a complete workflow for analyzing and predicting vegetation cover anomalies using GEOGLAM NRM regional reports. It integrates historical vegetation cover data, rainfall, and probabilistic models to assess the risk of low vegetation cover months.

---

## **Features**

- Load and preprocess GEOGLAM NRM regional report CSVs  
- Compute historical seasonal cycles and cover anomalies  
- Calculate 12-month rolling cumulative rainfall  
- Visualize:
  - Monthly cover summary vs historical statistics  
  - Full time series of vegetation cover  
  - Cover anomalies vs 12-month rainfall  
  - Logistic regression predictions with current risk highlighted  
- Fit OLS regression for rainfall-cover relationships  
- Forward-chaining logistic regression for probabilistic low-cover forecasting  
- Automatic risk assessment for the most recent month  

---

## **Getting Started**

### **1. Clone this repository**
```bash
git clone https://github.com/u8008892/nrm_vegetation_cover_ews.git
cd nrm_vegetation_cover_ews
```

### **2. Install dependencies**
```bash
pip install -r requirements.txt
```

### **3. Prepare your data**
Download your regional report CSV from GEOGLAM and save it locally.

In the notebook, update the placeholder with the path to your CSV:

```python
csv_file = "PATH_TO_YOUR_DOWNLOADED_NRM_REGIONAL_REPORT.csv"
```

### **4. Run the notebook**

Open the notebook in Jupyterand run cells sequentially. Each cell builds on the previous:

1. Import libraries & define configuration
2. Load and preprocess CSV
3. Compute seasonal cycles & anomalies
4. Generate visualizations
5. Fit OLS regression
6. Run forward-chaining logistic regression
7. Assess current risk
