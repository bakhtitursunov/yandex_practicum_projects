# 🛢️ Oil Field Profitability Prediction

This project focuses on helping the oil company **GlavRosGosNeft** determine the most profitable region to drill new oil wells. Using data from geological surveys and machine learning models, we aim to identify the region with the highest expected profit and lowest financial risk.

---

## 📌 Project Objective

- Predict the volume of oil reserves in new wells based on available geological features
- Evaluate profitability and associated risks for three regions using bootstrapping
- Recommend the optimal region for investment and oil field development

---

## 📊 Dataset Description

Geological survey data from **three different regions** are provided. Each dataset contains:

| Column | Description |
|--------|-------------|
| `id`   | Unique identifier of the oil well |
| `f0`, `f1`, `f2` | Features of the geological location |
| `product` | Volume of oil reserves in thousand barrels (target variable) |

**Files:**

- `geo_data_0.csv`
- `geo_data_1.csv`
- `geo_data_2.csv`

---

## 📈 Project Workflow

### 1. Data Preparation

- Loaded data from all three regions
- Verified for null values and consistent formatting
- Checked feature-target correlations

### 2. Model Training and Evaluation

For each region:

- Split data into training (75%) and validation (25%) sets
- Trained a **Linear Regression** model
- Calculated RMSE (Root Mean Squared Error)
- Printed the **mean predicted reserves** and compared with actuals

### 3. Profit Calculation Setup

Key assumptions:

- **500 wells** explored per region; **200** best wells selected
- **Revenue per 1k barrels:** 450,000 RUB
- **Budget per region:** 10 billion RUB
- **Break-even point** calculated from cost-to-revenue ratio

Analyzed:
- Minimum required volume per well
- Average predicted volume per region

### 4. Revenue Simulation Function

Created a function to:

- Select top 200 wells based on model predictions
- Sum actual reserves from those wells
- Calculate expected profit

### 5. Risk and Profit Analysis with Bootstrapping

- Applied **Bootstrapping (1000 iterations)** per region
- Computed:
  - Mean profit
  - 95% confidence interval
  - Risk of loss (probability of negative profit)

### 6. Region Recommendation

Based on results:

- Chose the region with:
  - **Highest average profit**
  - **Risk of loss < 2.5%**

---

## 📊 Key Results

| Region | Mean Profit (₽ bln) | 95% CI (₽ bln)        | Risk of Loss |
|--------|---------------------|------------------------|--------------|
| 0      | 396 ± 111           | [273, 507]             | 6.2% ❌       |
| 1      | 445 ± 97            | [347, 542]             | 0.8% ✅       |
| 2      | 429 ± 99            | [330, 528]             | 1.0% ✅       |

✅ **Recommended Region: Region 1** — Highest average profit and acceptable risk level.

---

## 💡 Business Insights

- **Linear regression** performed best in Region 1 and yielded stable profit forecasts.
- **Region 1** should be prioritized for new drilling projects due to its:
  - Low risk of loss (<1%)
  - Strong average profitability
- **Region 0** carries higher risk (>5%) and should be avoided unless more data becomes available or risk tolerance increases.

---

## 🗃️ Files Included

- `notebook.ipynb` — Full analysis and modeling workflow  
- `data/` — Folder with all region datasets  
- `README.md` — Project description and results summary  

---

## 🛠 Technologies Used

- Python, pandas, NumPy  
- scikit-learn (LinearRegression, train_test_split, metrics)  
- Matplotlib, Seaborn  
- Bootstrap sampling  
- Git / GitHub

---
