# 🏭 Predicting Alloy Temperature at Steelworks

**Project Type**: Final Exam Project — Industrial Use Case  
**Company**: "Stalnaya Ptitsa" Steelworks  
**Objective**: Predict the **temperature of molten alloy** during steel processing to help reduce **electricity consumption** and optimize production costs.

---

## 🎯 Business Goal

"Stalnaya Ptitsa" steelworks seeks to minimize energy consumption during the **ladle furnace stage** of steel treatment. To achieve this, the company aims to build a **machine learning model** that can **predict the temperature** of the molten alloy based on various process parameters.

Such a model can later be used in **technological simulations** of the metallurgical process, improving planning and efficiency.

---

## 🔍 Process Overview

The process involves:

- Heating steel inside **refractory-lined ladles** using **graphite electrodes**.
- Removing sulfur (desulfurization), adjusting the chemical composition, and sampling.
- Adding alloying materials via:
  - **bulk feeders** (powders, granules),
  - **wire feeding systems** (tribe units).
- Repeated **temperature and chemical measurements** after alloying and gas purging.
- Final casting of the alloy into semi-finished slabs (slabs).

---

## 🧾 Data Sources

The dataset consists of multiple CSV files, each describing different process aspects. All files share a common column `key`, representing a unique batch ID.

| File                        | Description                                       |
|-----------------------------|---------------------------------------------------|
| `data_arc_new.csv`          | Electrode usage: start/end times, power metrics   |
| `data_bulk_new.csv`         | Volume of bulk alloying materials (Bulk 1–15)     |
| `data_bulk_time_new.csv`    | Timing of bulk material additions                 |
| `data_gas_new.csv`          | Volume of inert gas purging (Gas 1)               |
| `data_temp_new.csv`         | Alloy temperature measurements over time          |
| `data_wire_new.csv`         | Volume of wire alloying materials (Wire 1–9)      |
| `data_wire_time_new.csv`    | Timing of wire material additions                 |

> ⚠️ A single batch (`key`) may have multiple rows representing different iterations of the process.

---

## 🧭 Project Workflow

### Step 1: Load and Inspect Data
- Import CSV files and conduct basic sanity checks.
- Explore unique batch counts, missing values, and time formats.

### Step 2: Exploratory Data Analysis (EDA)
- Analyze and visualize each dataset separately.
- Identify useful features for modeling and discard irrelevant or noisy ones.

### Step 3: Data Merging
- Merge all cleaned features into a single DataFrame using the `key` column.

### Step 4: Post-Merge EDA
- Conduct correlation analysis and distribution plots.
- Generate new features based on domain knowledge and time-based metrics.

### Step 5: Data Preparation
- Encode categorical features (if any), normalize numerical values.
- Split data into **training** and **test** sets.

### Step 6: Model Training
- Train **at least two machine learning models**:
  - e.g., Linear Regression, Random Forest, Gradient Boosting
- Perform **hyperparameter tuning** on at least one model.

### Step 7: Model Evaluation
- Compare models based on **RMSE** and overall predictive performance.
- Evaluate final model on test data.

### Step 8: Final Report & Recommendations
- Summarize results and key insights.
- Provide actionable recommendations to optimize steel processing.

---

## 📊 Target Variable

- `Температура` (Temperature): Measured in degrees Celsius, this is the variable the model aims to predict.

---

## ⚙️ Technologies Used

- **Python**  
- pandas, NumPy, matplotlib, seaborn  
- scikit-learn  
- LightGBM or XGBoost (optional for ensemble modeling)  
- Jupyter Notebook  

---

## 📈 Evaluation Metric

- **Root Mean Squared Error (RMSE)**

\[
RMSE = \sqrt{\frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2}
\]

- The lower the RMSE, the better the model.

---

## ✅ Conclusion

- Built a regression model that accurately predicts the temperature of molten steel during production.
- Enabled simulation of the heating/alloying process to reduce **electricity usage**.
- Provided insights into the impact of different process parameters on temperature.
- Recommendation: deploy the model in a simulation environment and integrate with SCADA/MES systems for real-time monitoring and optimization.

---
