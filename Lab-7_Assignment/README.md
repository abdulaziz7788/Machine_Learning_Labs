# Lab-7 Assignment: Logistic Regression

## Files in this folder

- `02-Logistic Regression Assignment_Solved.ipynb` — completed Jupyter Notebook.
- `advertising.csv` — dataset used by the notebook.
- `README.md` — explanation of the solution.

## Dataset

The dataset is `advertising.csv`. It contains information about users and whether they clicked on an advertisement.

Important columns used in the model:

- `Daily Time Spent on Site`
- `Age`
- `Area Income`
- `Daily Internet Usage`
- `Male`
- Target column: `Clicked on Ad`

Text/date columns such as `Ad Topic Line`, `City`, `Country`, and `Timestamp` were not used in the basic logistic regression model because the assignment allows choosing columns, and numeric columns are easier and suitable for this lab.

## Solution steps

1. Imported the required libraries: pandas, NumPy, matplotlib, seaborn, and scikit-learn.
2. Loaded the dataset into a DataFrame named `ad_data`.
3. Displayed the first rows using `head()`.
4. Checked the dataset using `info()` and `describe()`.
5. Created exploratory data analysis plots:
   - Age histogram
   - Jointplot of Age vs Area Income
   - KDE jointplot of Age vs Daily Time Spent on Site
   - Jointplot of Daily Time Spent on Site vs Daily Internet Usage
   - Pairplot colored by `Clicked on Ad`
6. Selected numeric features for training.
7. Split the data into training and testing sets using `train_test_split`.
8. Trained a Logistic Regression model.
9. Predicted the test data results.
10. Evaluated the model using:
    - Classification report
    - Confusion matrix
    - Accuracy score

## How to run

Open the notebook in Jupyter Notebook, JupyterLab, or VS Code, then run all cells from top to bottom.

Make sure `advertising.csv` is in the same folder as the notebook.

## Required libraries

```bash
pip install pandas numpy matplotlib seaborn scikit-learn notebook
```
