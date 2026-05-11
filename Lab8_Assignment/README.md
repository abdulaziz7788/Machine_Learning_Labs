# Lab 8 Assignment

## Overview
This folder contains the README for Lab 8. The assignment follows the same machine learning workflow used in the previous solved labs.

## Objective
The goal of this lab is to build a machine learning model, train it using the provided dataset, and evaluate its performance using proper evaluation metrics.

## Dataset
The dataset should be placed in the same folder as the notebook before running the code.

Example:
```text
Lab8_Assignment/
│── Lab8_Assignment.ipynb
│── dataset.csv
│── README.md
```

## Steps Performed
The assignment solution should include the following steps:

1. Import the required libraries.
2. Load the dataset using pandas.
3. Explore the dataset using:
   - `head()`
   - `info()`
   - `describe()`
4. Check for missing values.
5. Separate the features and target variable.
6. Split the data into training and testing sets.
7. Train the machine learning model.
8. Make predictions on the test data.
9. Evaluate the model using appropriate metrics.
10. Display the final results.

## Libraries Used
```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

from sklearn.model_selection import train_test_split
from sklearn.metrics import classification_report, confusion_matrix, accuracy_score
```

## Common Machine Learning Workflow
```python
# Load data
df = pd.read_csv("dataset.csv")

# Split features and target
X = df.drop("target", axis=1)
y = df["target"]

# Train/test split
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.30, random_state=101
)

# Train model
model.fit(X_train, y_train)

# Predictions
predictions = model.predict(X_test)

# Evaluation
print(confusion_matrix(y_test, predictions))
print(classification_report(y_test, predictions))
print(accuracy_score(y_test, predictions))
```

## Notes
- Make sure the dataset file is in the same folder as the notebook.
- If the dataset has categorical columns, convert them using encoding before training.
- If the model requires scaling, use `StandardScaler`.
- The final notebook should contain both code and outputs.

## Result
The model should be trained and evaluated successfully, with the final performance shown using a confusion matrix and classification report.
