# 🧼 Toxic Comment Classification for WikiShop

**WikiShop**, an online marketplace, is launching a new feature that allows users to collaboratively edit and comment on product descriptions, similar to wiki platforms. To maintain a healthy and respectful community, the company needs a tool to automatically detect toxic comments and send them for moderation.

This project aims to train a classification model that can identify whether a comment is **toxic** or **non-toxic**.

> 📌 **Note**: The dataset is not included in this repository due to storage and licensing constraints.

---

## 🎯 Objective

Develop a machine learning model that classifies user comments as either **toxic** or **non-toxic**, based on their content.

The model must achieve an **F1 score of at least 0.75** on the validation/test set.

---

## 🧭 Project Workflow

1. **Data Loading and Exploration**
   - Load the dataset from `/datasets/toxic_comments.csv`.
   - Explore class balance and distribution of comment lengths.
   - Check for missing values and clean the data if necessary.

2. **Text Preprocessing**
   - Convert text to lowercase.
   - Remove punctuation, special characters, and stop words.
   - Apply lemmatization or stemming.
   - Tokenize and vectorize the text using methods such as:
     - CountVectorizer
     - TF-IDF
     - (Optionally) Word Embeddings or BERT

3. **Model Training and Evaluation**
   - Train multiple models, including:
     - Logistic Regression
     - Random Forest
     - Support Vector Machine
     - (Optional) BERT-based Transformer
   - Use cross-validation and grid/randomized search for hyperparameter tuning.
   - Evaluate performance using:
     - **F1 Score** (main metric)
     - Accuracy, Precision, Recall (for reference)

4. **Model Selection**
   - Compare models and select the best one based on:
     - F1 score (target ≥ 0.75)
     - Inference time
     - Interpretability

---

## 📈 Target Metric

The classification performance is measured using the **F1 Score**, which balances **Precision** and **Recall**:

\[
F1 = 2 \cdot \frac{Precision \cdot Recall}{Precision + Recall}
\]

Where:
- **Precision** = TP / (TP + FP)
- **Recall** = TP / (TP + FN)

> A successful model should have F1 ≥ 0.75.

---

## 🗃️ Dataset Description

File: `/datasets/toxic_comments.csv`

| Column   | Description                     |
|----------|---------------------------------|
| `text`   | User-submitted comment          |
| `toxic`  | Target variable:                |
|          | `1` – toxic comment             |
|          | `0` – non-toxic comment         |

---

## ⚙️ Technologies Used

- Python
- pandas, NumPy
- nltk, spaCy (for NLP preprocessing)
- scikit-learn
- LightGBM, CatBoost, XGBoost
- (Optional) HuggingFace Transformers (for BERT)
- Jupyter Notebook

---
