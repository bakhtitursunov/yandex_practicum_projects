# 🚖 Taxi Demand Forecasting

This project was developed for the company **"Chyotenkoye Taxi"**, which aims to improve service availability by forecasting hourly demand for taxi rides at airports. The company collected historical data on taxi orders and wants to attract more drivers during peak hours by using demand prediction.

The goal is to build a time series forecasting model that predicts the number of taxi orders for the next hour.

---

## 🎯 Project Objectives

- Build a model to predict the number of taxi orders for the next hour.
- Use historical hourly data and resample the dataset accordingly.
- Evaluate models using **Root Mean Squared Error (RMSE)**.
- Meet the success criterion:  
  **RMSE ≤ 48** on the test dataset.

---

## 🧭 Project Workflow

1. **Data Loading and Preparation**
   - Load the dataset from `/datasets/taxi.csv`.
   - Perform **resampling** to hourly intervals.
   - Check for missing values and handle them appropriately.

2. **Exploratory Data Analysis (EDA)**
   - Visualize time series trends and seasonality.
   - Detect outliers and patterns in demand.

3. **Feature Engineering**
   - Generate time-based features (e.g., hour, day of week, lag features).
   - Create rolling means or other aggregated indicators if needed.

4. **Model Training and Evaluation**
   - Train various models with different hyperparameters, such as:
     - **Linear Regression**
     - **Random Forest**
     - **Gradient Boosting**
     - **CatBoost / LightGBM**
   - Split the data:
     - Use the last **10%** of the data for the **test set**.
   - Evaluate model performance using **RMSE**.

5. **Model Selection**
   - Compare models by performance on the test set.
   - Choose the best model based on lowest RMSE and operational speed.

---

## 📈 Target Metric

The performance of all models is evaluated using the **Root Mean Squared Error (RMSE)**:

\[
\text{RMSE} = \sqrt{\frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2}
\]

Where:
- \( y_i \) is the actual number of orders
- \( \hat{y}_i \) is the predicted number of orders
- \( n \) is the number of observations

---

## 🗃️ Dataset Description

File: `/datasets/taxi.csv`

| Column       | Description                          |
|--------------|--------------------------------------|
| `num_orders` | Number of taxi orders per timestamp  |

> The dataset contains historical time series data. The index represents timestamps.

---

## ⚙️ Technologies Used

- Python
- pandas, NumPy
- scikit-learn
- LightGBM / CatBoost
- Matplotlib, Seaborn
- Jupyter Notebook

---

