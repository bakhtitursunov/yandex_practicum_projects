# 🛍️ Personalized Customer Retention Strategy

**Project #06** | Predicting customer activity decline and segmenting clients for targeted marketing  
**Category:** Classification, Customer Segmentation, Business Strategy  
**Tools:** Python, pandas, matplotlib, seaborn, scikit-learn, SHAP, pipelines, GridSearchCV

---

## 📌 Project Overview

This project focuses on developing a data-driven solution to help the online store *"V odin klik"* improve customer retention. As acquiring new users becomes less effective, the company aims to personalize offers for existing customers based on their likelihood to reduce purchasing activity.

The task involves:
- Predicting a customer's probability of decreasing activity in the next 3 months.
- Analyzing customer segments using behavioral and profitability data.
- Creating tailored marketing strategies for each segment.

The goal is to ensure more efficient communication, reduce churn, and maximize customer lifetime value.

---

## 🔍 Project Tasks

1. **Data Loading & Preprocessing**  
   - Merged multiple sources of customer data: site behavior, marketing interactions, financial metrics, and profitability.
   - Cleaned and formatted data, handled delimiters and decimal separators.

2. **Exploratory Data Analysis (EDA)**  
   - Analyzed features affecting activity, such as number of pages visited, service type, errors, promotions, etc.
   - Filtered out users with less than 3 months of activity.

3. **Feature Engineering & Aggregation**  
   - Converted transactional time-series into wide format features per period (current and past months).
   - Merged all features into one modeling dataset.

4. **Correlation & Multicollinearity Check**  
   - Identified highly correlated numeric features.
   - Removed or transformed redundant features to avoid multicollinearity.

5. **Model Building & Evaluation**  
   - Created pipelines with `ColumnTransformer` for encoding and scaling.
   - Trained and tuned 4 models:  
     - `KNeighborsClassifier`  
     - `DecisionTreeClassifier`  
     - `LogisticRegression`  
     - `SVC`  
   - Selected the best model based on F1-score.

6. **Feature Importance Analysis**  
   - Used SHAP values to interpret key drivers of customer behavior.
   - Identified the most influential features (e.g., promo purchases, errors, time on site).

7. **Customer Segmentation & Strategy**  
   - Combined prediction results with profitability data.
   - Defined actionable customer segments for targeted campaigns.

---

## 📊 Key Results

- **Best Model:** `LogisticRegression` with optimized threshold  
- **F1-score (test set):** 0.81  
- **Top 3 impactful features (via SHAP):**  
  - Number of promo purchases  
  - Errors experienced on site  
  - Average time spent per visit  

---

## 👥 Segment Analysis & Recommendations

### 📌 Selected Segment:  
**High promo purchase ratio + high probability of decreased activity**

- **Insight:** These customers are highly price-sensitive and primarily buy during discounts.  
- **Issue:** If promotions decrease or become less appealing, these customers are likely to churn.  
- **Profitability:** Medium-to-high average monthly profit.

### ✅ Strategic Recommendations:
- **Retargeting Campaigns:** Focused promotions with limited-time offers for their preferred product categories.
- **Loyalty Program:** Introduce a point-based reward system for purchases made without discounts.
- **On-site Experience Optimization:** Highlight promo sections and personalized banners.

---

## 🧾 Conclusion

This project successfully combined behavioral, transactional, and profitability data to build a classification model and deliver actionable business insights.

- Developed a model to predict customer drop-off in activity with solid performance metrics.
- Identified behavioral and marketing features most associated with customer churn.
- Created a segmentation-based strategy to increase retention and maximize profit per user.

---

## 📁 Files

- `notebook.ipynb` — Jupyter Notebook with code and analysis  
- `data/` — Source datasets  
- `README.md` — This file  

---

## 🔧 Tech Stack

- Python (pandas, NumPy, matplotlib, seaborn, scikit-learn, SHAP)
- Jupyter Notebook
- Git / GitHub

---
