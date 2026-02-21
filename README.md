# Email Spam Classification - Exploratory Data Analysis (EDA)

This project applies Exploratory Data Analysis and Data Visualization techniques to a dataset of 5,728 emails. The goal is to identify patterns that distinguish **Spam** from **Ham** (legitimate) messages using Python's core data science stack.

## 🛠️ Libraries Used
The analysis is built strictly using the following modules:
* **NumPy**: For efficient numerical array operations.
* **Pandas**: For data cleaning, handling CSV files, and feature engineering.
* **Matplotlib**: For creating the foundational figure structures and boxplots.
* **Seaborn**: For advanced statistical visualizations and distribution plots.

---

## 🚀 Analysis Workflow

### 1. Data Cleaning (Lab 3: EDA)
To ensure high-quality data for future modeling, I performed the following:
* **Duplicate Removal**: Identified and removed **33 duplicate entries** found in the raw CSV.
* **Text Preprocessing**: Stripped the repetitive `"Subject: "` prefix from all email bodies to isolate the actual message content.
* **Null Check**: Verified that the dataset contains no missing values.

### 2. Feature Engineering
* **Character Count**: Created a `length` feature representing the total number of characters in each email string. This is a key metric for identifying automated spam patterns.

### 3. Data Visualization (Lab 1 & 2)
Using statistical graphics, I uncovered several key insights:
* **Class Imbalance**: Visualized the ratio of Spam vs. Ham using `sns.countplot`.
* **Length Distribution**: Used `sns.histplot` with a KDE (Kernel Density Estimate) to compare text length. Legitimate emails tend to have a broader distribution, while spam is often more concentrated.
* **Outlier Detection**: Generated boxplots to identify extreme outliers, noting that "Ham" emails often reach significantly higher character counts (up to 40k+ characters) than "Spam."

---

## 📊 Summary of Findings

| Metric | Ham (Legitimate) | Spam |
| :--- | :--- | :--- |
| **Count** | 4,327 | 1,368 |
| **Median Length** | ~1,113 chars | ~684 chars |
| **Max Length** | 43,943 chars | 28,423 chars |

**Conclusion**: Legitimate emails are generally longer and exhibit much higher variance in length compared to spam messages.

---

## 📂 Project Structure
* `Lab3.ipynb`: The main notebook containing the analysis code.
* `emails (1).csv`: The raw dataset.
* `cleaned_emails.csv`: The processed output file.
