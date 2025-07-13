# 👥 Employee Satisfaction & Attrition Prediction

**Project #07** | Predicting employee satisfaction scores and resignations  
**Category:** Regression, Classification, HR Analytics, Business Impact  
**Tools:** Python, pandas, scikit-learn, GridSearchCV, pipelines, matplotlib, seaborn

---

## 📌 Project Overview

The project was developed for the HR analytics department of the company *"Careful Jobs"*. The department provides data-driven insights to help businesses reduce employee turnover and prevent financial losses caused by unexpected resignations.

The solution includes two parts:
1. Predicting an employee's **job satisfaction level** (continuous score from 0 to 1).
2. Predicting the **probability of resignation** from the company.

Both tasks are addressed using real employee data and machine learning models with automated pipelines, custom metrics, and rigorous evaluation.

---

## 🔍 Business Objective

- **Why predict satisfaction?**  
  Job satisfaction is a key indicator of employee retention. Measuring it across the company via surveys is expensive and inefficient, especially for large workforces. A predictive model saves time and resources.

- **Why predict resignations?**  
  Sudden departures of critical employees cause operational disruptions. A predictive attrition model allows the company to proactively intervene and reduce turnover.

---

## 📊 Data Description

### Dataset 1 — Employee Satisfaction  
**Target:** `job_satisfaction_rate` — score from 0 to 1  
**Features:**
- `id` — employee ID  
- `dept` — department  
- `level` — job level  
- `workload` — workload level  
- `employment_years` — tenure in years  
- `last_year_promo` — promoted last year  
- `last_year_violations` — violations last year  
- `supervisor_evaluation` — manager's performance rating  
- `salary` — monthly salary  

### Dataset 2 — Employee Attrition  
**Target:** `quit` — binary flag for resignation  
**Same input features as above**, plus predicted satisfaction rate from Task 1.

---

## 📈 Task 1: Satisfaction Score Prediction (Regression)

### Steps:
1. **Data Preparation:**  
   - Preprocessed missing values in pipeline  
   - Encoded categorical variables using multiple encoders  
   - Scaled numeric features

2. **EDA:**  
   - Analyzed salary vs satisfaction  
   - Compared satisfaction across departments, levels, and tenure

3. **Model Training:**  
   - Trained multiple models: Linear Regression, Decision Tree Regressor  
   - Used `GridSearchCV` to tune hyperparameters  
   - Evaluated models using custom **SMAPE** metric

4. **Best Model:**  
   - Decision Tree Regressor with tuned depth  
   - Achieved **SMAPE ≤ 15%** on test data

---

## ✅ SMAPE Function (used in evaluation)

```python
def smape(y_true, y_pred):
    return np.mean(2 * np.abs(y_pred - y_true) / (np.abs(y_true) + np.abs(y_pred))) * 100

## 📉 Task 2: Employee Resignation Prediction (Classification)

### Steps:
1. **Data Preparation:**  
   - Merged predicted satisfaction scores from Task 1  
   - Encoded and scaled features using pipelines  
   - Filled missing values and treated categorical features

2. **EDA & Resignation Profiling:**  
   - Created profiles for employees who quit vs those who stayed  
   - Found that quitters were more likely to:
     - Have lower satisfaction scores  
     - Not be promoted recently  
     - Work in high-workload environments  
     - Have lower supervisor evaluations  
     - Earn less on average

3. **Correlation Analysis:**  
   - Verified strong relationship between `job_satisfaction_rate` and `quit`  
   - Visualized satisfaction score distributions for quit vs retained employees

4. **Model Training:**  
   - Trained multiple models: Logistic Regression, Random Forest, Gradient Boosting  
   - Tuned hyperparameters using grid search  
   - Evaluated models using **ROC-AUC** metric

5. **Best Model:**  
   - Gradient Boosting Classifier  
   - Achieved **ROC-AUC ≥ 0.91** on test data

---

## 📊 Feature Importance (Task 2)

Top contributing features to employee resignation:
- Predicted satisfaction score  
- Supervisor evaluation  
- Recent promotions  
- Salary  
- Violations  

---

## 💡 Business Recommendations

### For At-Risk Employees (High Probability of Resignation):
- **Targeted Retention Plans:**  
  Initiate one-on-one meetings with supervisors, offer flexible hours or job role reviews.
  
- **Promotion Path Transparency:**  
  Employees without recent promotions are more likely to quit — clearly define growth trajectories.

- **Performance & Feedback Alignment:**  
  Manager evaluations and job satisfaction show strong influence — train supervisors in people management.

- **Department-Level Monitoring:**  
  Departments with high attrition should be audited for management practices and workload balance.

---

## ✅ Final Conclusion

This two-part project successfully delivered models that predict employee satisfaction and resignation probability. The solution supports HR teams in reducing turnover through proactive and personalized retention strategies.

- The satisfaction model achieved strong SMAPE performance and is ready to replace periodic surveys.
- The attrition model identifies high-risk employees with ROC-AUC above 0.91, allowing for timely interventions.
- Additional features like predicted satisfaction significantly improve resignation prediction quality.

---

## 📁 Files

- `notebook.ipynb` — Full analysis and modeling code  
- `data/` — Datasets for both tasks  
- `README.md` — This file  

---

## 🔧 Technologies Used

- Python, pandas, NumPy  
- scikit-learn, GridSearchCV, pipelines  
- matplotlib, seaborn  
- Custom metrics (SMAPE)  
- Git / GitHub
