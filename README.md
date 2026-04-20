Lab 6: E-Commerce Product Pricing Analysis
💡 The Core Idea
The objective of this lab is to apply Regression Analysis to understand the dynamics of a competitive marketplace. Using the Olist e-commerce dataset, we focus on identifying the relationship between product attributes, pricing, and freight costs to predict the final price of an item.

The goal is to move beyond simple data exploration and build a model that can accurately estimate price points based on historical transaction features.

🧠 Key Machine Learning Concepts
Multivariate Regression: Analyzing how multiple independent variables (like freight value, product weight, and dimensions) collectively influence the target price.

Feature Engineering: Processing raw product dimensions (
length×height×width
) and weight to extract meaningful predictors for logistics-heavy pricing.

Correlation Mapping: Identifying the strength of the relationship between logistics costs (freight) and the actual product value to determine price elasticity.

Model Evaluation: Using metrics like Mean Absolute Error (MAE) and R-squared (
R 
2
 
) to quantify the accuracy of the price predictions.

🛠️ Technical Implementation
Data Integration: Merging product-level details with item-level transaction data to create a comprehensive training set.

Handling Sparsity: Cleaning and managing missing values within product categories and measurements to ensure model stability.

Dimensionality Impact: Assessing how physical product attributes significantly weight into the final cost structure in a real-world e-commerce environment.