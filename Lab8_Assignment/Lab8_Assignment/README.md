# Lab 8 Assignment - K Nearest Neighbors

## Overview
This lab solves the K Nearest Neighbors assignment using the provided `KNN_Project_Data` dataset. The goal is to train a KNN classification model, evaluate it, then improve it by choosing a better K value using the elbow method.

## Files Included

- `02-K Nearest Neighbors Assignment_SOLVED.ipynb` - completed assignment notebook
- `KNN_Project_Data` - dataset used in the assignment
- `01-K Nearest Neighbors.ipynb` - original practice/reference notebook
- `README.md` - explanation of the solution

## Dataset Used

The assignment uses:

```text
KNN_Project_Data
```

The target column is:

```text
TARGET CLASS
```

The feature columns are all other columns in the dataset.

## Steps Performed

1. Imported required libraries: pandas, numpy, matplotlib, seaborn, and scikit-learn.
2. Loaded the dataset using pandas.
3. Checked the first rows of the dataframe.
4. Created a pairplot using `TARGET CLASS` as the hue.
5. Standardized the feature variables using `StandardScaler`.
6. Converted scaled features into a new dataframe.
7. Split the data into training and testing sets using `train_test_split`.
8. Trained a KNN model with `n_neighbors=1`.
9. Generated predictions on the test set.
10. Evaluated the model using a confusion matrix and classification report.
11. Used the elbow method to test K values from 1 to 39.
12. Retrained the model using `k=17`.
13. Printed the final confusion matrix and classification report.

## Libraries Used

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

from sklearn.preprocessing import StandardScaler
from sklearn.model_selection import train_test_split
from sklearn.neighbors import KNeighborsClassifier
from sklearn.metrics import classification_report, confusion_matrix
```

## Final Model

The final model uses:

```python
KNeighborsClassifier(n_neighbors=17)
```

## Notes

Feature scaling is important for KNN because KNN depends on distance between points. Without scaling, features with larger values can dominate the distance calculation.

## Result

The assignment notebook is completed and includes the full KNN workflow: loading data, preprocessing, model training, prediction, evaluation, elbow method, and final retraining.
