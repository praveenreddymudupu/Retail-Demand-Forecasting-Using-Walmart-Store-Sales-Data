# Walmart Demand Forecasting using Machine Learning

##  Project Overview

This project focuses on building an end-to-end **Demand Forecasting** solution for Walmart using historical weekly sales data. The objective is to accurately predict weekly sales across multiple Walmart stores and departments by leveraging historical sales records, store information, promotional markdowns, holidays, and external economic factors.

The project demonstrates the complete machine learning workflow, including data preprocessing, exploratory data analysis (EDA), feature engineering, model development, hyperparameter tuning, model evaluation, and explainability using SHAP.

---

# Dataset

The dataset is the **Walmart Store Sales Forecasting** dataset from Kaggle.

Files used:

- **train.csv** – Historical weekly sales data
- **test.csv** – Test dataset for prediction
- **stores.csv** – Store information
- **features.csv** – External factors such as temperature, fuel price, CPI, unemployment, and markdowns

Dataset Source:

https://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting/data

---

# Project Objectives

- Forecast weekly sales for Walmart stores.
- Analyze seasonal sales patterns.
- Understand the impact of holidays and promotions.
- Compare multiple machine learning models.
- Select the best-performing model.
- Explain model predictions using SHAP.

---

# Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost
- Statsmodels (ARIMA)
- SHAP
- Jupyter Notebook

---

# Project Structure

```
Walmart-Demand-Forecasting/
│
├── data/
│   ├── train.csv
│   ├── test.csv
│   ├── stores.csv
│   └── features.csv
│
├── notebooks/
│   └── Walmart_Demand_Forecasting.ipynb
│
├── reports/
│   └── Process_Flow_Document.pdf
│
├── requirements.txt
│
├── README.md
```

---

# Project Workflow

1. Data Loading
2. Data Cleaning
3. Dataset Merging
4. Exploratory Data Analysis (EDA)
5. Feature Engineering
6. Train-Test Split
7. Feature Scaling
8. Model Training
9. Hyperparameter Tuning
10. Model Evaluation
11. SHAP Explainability
12. Business Insights

---

# Exploratory Data Analysis

The following analyses were performed:

- Weekly Sales Distribution
- Sales Trend Over Time
- Sales by Store Type
- Holiday vs Non-Holiday Sales
- Correlation Heatmap
- Temperature vs Weekly Sales
- Top 10 Stores by Sales

---

# Feature Engineering

The following features were created:

### Date Features

- Year
- Month
- Week
- Quarter
- DayOfWeek

### Holiday Features

- IsHoliday
- Holiday_Next_Week

### Lag Features

- Lag_1
- Lag_2
- Lag_4

### Rolling Statistics

- Rolling Mean
- Rolling Standard Deviation

### Store-Level Features

- Store Average Sales
- Department Average Sales

### Promotion Features

- Total MarkDown
- Average MarkDown
- Active MarkDown Count

### Interaction Features

- Temperature × Fuel Price
- Store Size × Total MarkDown

---

# Machine Learning Models

The following forecasting models were implemented:

- Linear Regression
- Random Forest Regressor
- XGBoost Regressor
- ARIMA

---

# Hyperparameter Tuning

Random Forest was optimized using **RandomizedSearchCV**.

Optimized Parameters:

- Number of Trees
- Maximum Depth
- Minimum Samples Split
- Minimum Samples Leaf
- Maximum Features

---

# Model Evaluation Metrics

The models were evaluated using:

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- Mean Absolute Percentage Error (MAPE)
- R² Score

---

# Model Explainability

SHAP (SHapley Additive Explanations) was used to interpret model predictions.

Generated Visualizations:

- SHAP Summary Plot
- SHAP Feature Importance
- Feature Importance Chart

---

# Business Insights

- Holiday weeks significantly increase sales.
- Promotional markdowns positively influence demand.
- Historical sales (lag features) are the strongest predictors.
- Larger stores generally generate higher sales.
- XGBoost achieved the best forecasting performance.

---

# Future Improvements

- Implement LightGBM and CatBoost.
- Develop an LSTM-based forecasting model.
- Deploy the model using Streamlit.
- Integrate real-time prediction APIs.
- Automate retraining with MLOps pipelines.

---

# How to Run

### Clone the repository

```bash
git clone https://github.com/yourusername/Walmart-Demand-Forecasting.git
```

### Navigate to the project directory

```bash
cd Walmart-Demand-Forecasting
```

### Install dependencies

```bash
pip install -r requirements.txt
```

### Launch Jupyter Notebook

```bash
jupyter notebook
```

Open:

```
Walmart_Demand_Forecasting.ipynb
```

Run all cells sequentially.

---

# Results

Among all evaluated models:

- **XGBoost** achieved the best overall performance.
- Random Forest performed competitively after hyperparameter tuning.
- Linear Regression served as the baseline model.
- ARIMA captured time-series trends but was less effective than XGBoost for this dataset.

---

#  Author

**Praveen Reddy**

Walmart Demand Forecasting Project
