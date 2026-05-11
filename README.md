# Lab11_Assignment - Credit Card Customer Segmentation

This folder contains the solved assignment notebook for the credit card customer segmentation task using K-Means clustering.

## Files

- `02-Credit Card Customer Segmentation Assignment_SOLVED.ipynb` - completed assignment notebook.
- `CC_GENERAL.csv` - dataset used by the notebook.
- `credit_card_segmentation_solution.py` - Python script version of the notebook solution.
- `cluster_summary.csv` - mean feature values for each final cluster.
- `cluster_counts.csv` - number of customers in each cluster.
- `elbow_inertia_values.csv` - inertia values for K = 1 to 10.
- `silhouette_scores.csv` - silhouette scores for K = 2 to 10.
- `screenshots/` - exported figures from the assignment.

## What the assignment does

1. Imports the required libraries.
2. Loads `CC_GENERAL.csv`.
3. Checks the dataset using `head()`, `shape`, `info()`, and `describe()`.
4. Drops `CUST_ID` because it is an ID column, not a behavioral feature.
5. Checks missing values.
6. Fills missing values using mean imputation.
7. Creates histograms, a correlation heatmap, and scatter plots.
8. Scales the features using `StandardScaler`.
9. Uses the elbow method and silhouette score to compare K values.
10. Trains the final K-Means model with `K = 4`.
11. Adds cluster labels to the dataframe.
12. Creates cluster summary and customer count tables.
13. Uses PCA to visualize the final clusters in 2D.
14. Answers the final assignment questions.

## Final K value

The final selected K value is **4**. The elbow curve begins to slow down around K = 4. The sampled silhouette score is highest at K = 3, but K = 4 gives more useful business segments while still being reasonable.

## Missing values

The dataset had missing values in:

- `CREDIT_LIMIT`: 1 missing value
- `MINIMUM_PAYMENTS`: 313 missing values

They were handled using mean imputation.

## Final cluster interpretation

- **Cluster 0:** Regular purchase customers with moderate balance and purchases.
- **Cluster 1:** High-value/high-spending customers with very high purchases and high payments.
- **Cluster 2:** Customers who rely heavily on cash advance and have high balances.
- **Cluster 3:** Low-activity customers with lower purchases and generally lower usage.

## How to run

Open the solved notebook in Jupyter Notebook or JupyterLab and run all cells from top to bottom. Make sure `CC_GENERAL.csv` is in the same folder as the notebook.
