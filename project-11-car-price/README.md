# 🚗 Car Price Prediction App

This project is developed for the used car sales service **"Not Crashed, Not Repainted"**, which is building a mobile app to help users estimate the market value of their vehicles based on technical specifications and historical sales data.

The goal is to build a machine learning model that accurately predicts car prices while keeping training and prediction times reasonable.

> 📌 **Note**: The dataset is not included in this repository due to storage and licensing constraints.

---

## 🎯 Project Objectives

- Predict the market price of a used car.
- Compare multiple machine learning models based on:
  - Prediction accuracy (RMSE)
  - Training time
  - Prediction time
- Select the best-performing model according to business requirements.

**Success Criterion:**  
RMSE < 2500 on the test set.

---

## 📈 Project Workflow

1. **Data Loading and Exploration**
   - Load the dataset from `/datasets/autos.csv`.
   - Analyze and clean the data.
   - Handle missing values and anomalies.
   - Remove non-informative features (e.g., `NumberOfPictures`).

2. **Data Preprocessing**
   - Encode categorical features.
   - Split the data into training, validation, and test sets.

3. **Model Training**
   - Train and tune several models:
     - **Gradient Boosting with LightGBM**
     - **Linear Regression**
     - **Random Forest**
     - (Other simple models for comparison)
   - Measure and compare:
     - RMSE
     - Training time
     - Prediction time

4. **Model Selection**
   - Choose the best model based on:
     - Lowest RMSE
     - Fast performance
     - Business constraints

5. **Final Evaluation**
   - Validate the selected model on the test set.
   - Confirm performance meets expectations.

---

## 🧪 Target Metric

The project uses **Root Mean Squared Error (RMSE)** to evaluate model performance.

\[
\text{RMSE} = \sqrt{\frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2}
\]

Where:
- \( y_i \) is the actual price
- \( \hat{y}_i \) is the predicted price
- \( n \) is the number of samples

---

## 🗃️ Dataset Description

File: `/datasets/autos.csv`

| Feature              | Description                              |
|----------------------|------------------------------------------|
| `DateCrawled`        | Date the ad was crawled from the site    |
| `VehicleType`        | Type of car body                         |
| `RegistrationYear`   | Year the car was registered              |
| `Gearbox`            | Gearbox type (manual/automatic)          |
| `Power`              | Engine power in HP                      |
| `Model`              | Car model                                |
| `Kilometer`          | Mileage in kilometers                    |
| `RegistrationMonth`  | Month of registration                    |
| `FuelType`           | Fuel type (petrol, diesel, etc.)         |
| `Brand`              | Car brand                                |
| `Repaired`           | Whether the car has been repaired        |
| `DateCreated`        | Date the ad was created                  |
| `NumberOfPictures`   | Number of pictures in the ad             |
| `PostalCode`         | Postal code of the seller                |
| `LastSeen`           | Date the user was last active            |
| `Price` (target)     | Selling price in euros                   |

---

## ⚙️ Technologies Used

- **Python**
- **pandas**, **NumPy**
- **scikit-learn**
- **LightGBM**
- **Matplotlib**, **Seaborn**
- **Jupyter Notebook**

---
