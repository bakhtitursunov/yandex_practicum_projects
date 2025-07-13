# 🧑‍🦳 Age Prediction from Facial Photos for Retail Analytics

**Khlebnaya-Sol** supermarket chain is implementing a computer vision system to analyze checkout area photos. The goal is to estimate the approximate **age of customers** from facial images in order to:

- Analyze purchase behavior by age group.
- Monitor compliance with alcohol sales regulations.

This project aims to train a **convolutional neural network (CNN)** that can estimate a person’s age based on their photo.

> 📌 **Note**: The dataset is not included in this repository due to storage and licensing constraints.

---

## 🎯 Objective

Build and train a machine learning model that predicts a person’s **real age** from a facial image.

---

## 🧭 Project Workflow

1. **Exploratory Data Analysis (EDA)**
   - Explore image resolution, distribution of age labels, and sample imbalance.
   - Visualize sample images and assess data quality.

2. **Data Preparation**
   - Use `ImageDataGenerator.flow_from_dataframe()` to load and preprocess image data.
   - Normalize image pixel values and resize images for training.
   - Split data into training, validation, and test sets.

3. **Model Architecture**
   - Construct a convolutional neural network (CNN) using:
     - Keras Sequential API or Functional API
     - Batch normalization and dropout layers to improve generalization
   - Optionally, use a pre-trained model (e.g., MobileNetV2, ResNet50) for transfer learning.

4. **Training**
   - Compile the model using `mean absolute error (MAE)` as the loss function.
   - Monitor training and validation metrics over epochs.
   - Use callbacks (e.g., `EarlyStopping`, `ModelCheckpoint`) to prevent overfitting.

5. **Evaluation**
   - Evaluate final model performance on a separate test set.
   - Report key metrics such as MAE or RMSE.
   - Visualize prediction vs. true age for qualitative analysis.

---

## 📁 Data Description

The original dataset comes from the **ChaLearn Looking at People** dataset.

- **Image folder**: `/datasets/faces/final_files/`
  - Contains facial images in `.jpg` format.

- **CSV file**: `labels.csv`
  - Contains two columns:
    | Column     | Description                  |
    |------------|------------------------------|
    | `file_name` | Name of the image file       |
    | `real_age`  | Actual age of the person     |

---

## 📊 Evaluation Metric

The main evaluation metric is **Mean Absolute Error (MAE)** between predicted and actual ages:

\[
MAE = \frac{1}{n} \sum_{i=1}^{n} |y_i - \hat{y}_i|
\]

Where:
- \( y_i \): actual age
- \( \hat{y}_i \): predicted age

---

## ⚙️ Technologies Used

- Python
- pandas, NumPy, matplotlib
- TensorFlow / Keras
- OpenCV / PIL (for image preprocessing)

---

## 📌 Notes

- The dataset is not included in this repository. You may download it manually from the [ChaLearn LAP website](https://chalearnlap.cvc.uab.cat/).
- This project focuses on **regression**, not classification.
- Ethical use of facial recognition and biometric analysis is crucial — always follow local privacy and data protection regulations.

---

## ✅ Conclusion

The trained CNN model helps estimate customer age from photos, allowing the retail business to:
- Tailor marketing and product offers.
- Enforce age-sensitive purchase policies more effectively.

This solution forms part of a broader retail intelligence system powered by computer vision.

---
