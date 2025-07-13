# 💳 Credit Payment Analysis

## 📌 Project Overview

The client is the credit department of a bank. The goal is to analyze whether a client's family status and number of children affect their ability to repay a loan on time. The input data includes statistics on customer solvency provided by the bank.

The results of this analysis will be considered when developing a credit scoring model — a system designed to evaluate the ability of a potential borrower to repay a loan.

## 📁 Project Contents

- `credit_payment_analysis.ipynb` — main notebook with data processing, analysis, and conclusions.
- `description.docx` — task instructions.
- `data/credit_data.csv` — dataset from the bank.

## 📊 Dataset Description

| Column             | Description                                      |
|--------------------|--------------------------------------------------|
| `children`         | Number of children in the family                 |
| `days_employed`    | Total work experience in days                    |
| `dob_years`        | Client's age in years                            |
| `education`        | Education level                                  |
| `education_id`     | Identifier of education level                    |
| `family_status`    | Marital status                                   |
| `family_status_id` | Identifier of marital status                     |
| `gender`           | Gender                                           |
| `income_type`      | Employment type                                  |
| `debt`             | Whether the client had any unpaid debts         |
| `total_income`     | Monthly income                                   |
| `purpose`          | Purpose of the loan                              |

## 🧠 Key Aspects to Consider

During the analysis, the following aspects are addressed:

- Detection and description of data issues (missing values, duplicates, incorrect types)
- Techniques for data type conversion, missing value imputation, and duplicate handling
- Data categorization and feature transformation
- Clean code, logical structure, and clear step-by-step explanations
- Well-documented conclusions based on the data

## 🛠 Tools & Technologies

- Python
- Pandas
- Jupyter Notebook

---
