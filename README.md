# 📧 Email Spam Detection: Data Preprocessing (Lab 4)

This repository contains the implementation of **Data Quality Assessment and Preprocessing** techniques applied to the `emails.csv` dataset, as required for the **ARTI308 - Machine Learning** course.

---

## 🛠 Project Overview
The goal of this project is to transform raw, high-dimensional text data into a clean, normalized format suitable for machine learning training. The workflow follows the five core tasks outlined in Lab 4.

## 📋 Assignment Tasks

### **Task 1: Data Quality Assessment**
We performed an audit to identify inconsistencies in the raw data.
* **Feature Engineering:** Since raw text is non-numeric, we extracted `text_length` and `word_count` to allow for mathematical assessment.
* **Audit Results:** Checked for data types and missing values. The dataset was found to be structurally complete but required scaling due to the high variance in email lengths.

### **Task 2: Missing Value Strategy**
To ensure the dataset is robust against potential data loss, we implemented a handling strategy:
* **Applied Strategy:** **Mean Imputation**.
* **Rationale:** For numerical features like email length, replacing nulls with the average (mean) maintains the statistical integrity of the dataset without reducing the sample size.


### **Task 3: Outlier Detection & Handling (IQR)**
Extreme values can negatively impact model performance. We used the **Interquartile Range (IQR)** method to filter noise.
* **Calculation:** Bounds were set at $[Q1 - 1.5 \times IQR, Q3 + 1.5 \times IQR]$.
* **Action:** Removed outliers that fell outside these bounds to ensure the model focuses on representative email patterns.


[Image of box plot showing interquartile range and outliers]


### **Task 4: Feature Normalization**
Because `text_length` and `word_count` exist on different scales, we applied two normalization techniques:
1.  **Min-Max Scaling:** Rescales features to a range of $[0, 1]$.
2.  **Z-score Normalization (Standardization):** Centers data around a mean of $0$ with a standard deviation of $1$.
* **Importance:** This prevents features with larger numerical ranges from dominating the learning process.

### **Task 5: PCA & Explained Variance**
We applied **Principal Component Analysis (PCA)** to reduce the complexity of the dataset.
* **Analysis:** Our first Principal Component (**PC1**) captured approximately **92%** of the total variance.
* **Conclusion:** This high variance ratio confirms that we can simplify our data into a lower-dimensional space while retaining nearly all critical information.


---

## 💻 Tech Stack
* **Language:** Python 3.10+
* **Data Analysis:** Pandas, NumPy
* **Machine Learning:** Scikit-learn (Preprocessing, PCA)
* **Visualization:** Matplotlib, Seaborn

---

