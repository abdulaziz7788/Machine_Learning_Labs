# Support Vector Machine (SVM) Assignment

## Overview

This lab focuses on implementing a Support Vector Machine (SVM) model using Python and Scikit-learn. The Iris dataset is used to train and evaluate the classifier.

The assignment demonstrates:

* Data visualization
* Data preprocessing
* Training an SVM classifier
* Model evaluation
* Hyperparameter tuning using GridSearchCV

---

## Dataset

The lab uses the famous Iris dataset provided by Scikit-learn.

Features included:

* Sepal Length
* Sepal Width
* Petal Length
* Petal Width

Target classes:

* Setosa
* Versicolor
* Virginica

---

## Libraries Used

```python
pandas
numpy
matplotlib
seaborn
scikit-learn
```

---

## Steps Performed

### 1. Import Libraries and Dataset

The dataset is loaded into a Pandas DataFrame for analysis and visualization.

---

### 2. Data Visualization

Several visualizations are created using Seaborn:

* Pairplot of all features
* KDE plot for Setosa species

These plots help understand the relationships between features.

---

### 3. Train-Test Split

The dataset is divided into:

* Training set (70%)
* Testing set (30%)

using `train_test_split()`.

---

### 4. Training the SVM Model

An SVM classifier is created using:

```python
SVC()
```

The model is trained using the training dataset.

---

### 5. Predictions and Evaluation

Predictions are made on the test dataset.

The following evaluation metrics are used:

* Confusion Matrix
* Classification Report

These metrics measure the model’s performance.

---

### 6. Hyperparameter Tuning

`GridSearchCV` is used to find the best parameters for:

* `C`
* `gamma`
* `kernel`

This improves model accuracy and performance.

---

## Results

The optimized SVM model achieved high classification accuracy on the Iris dataset after tuning the hyperparameters.

---

## Technologies Used

* Python
* Jupyter Notebook
* Scikit-learn
* Seaborn
* Matplotlib

---

## Conclusion

This assignment demonstrates how Support Vector Machines can be applied to classification problems. It also highlights the importance of visualization, model evaluation, and hyperparameter tuning in machine learning workflows.
