# Marketing Campaign Analysis: The Four Ps

## 📌 Project Overview

Conducted a comprehensive Exploratory Data Analysis (EDA) on marketing campaign data, spanning data cleaning, imputation, and feature engineering. Validated hypotheses on consumer behavior, channel usage, and demographics. Delivered actionable insights through correlation heatmaps and visualizations to optimize product strategy and customer acquisition.

This project aligns with the widely utilized concept of the **Marketing Mix**, focusing on the Four Ps of marketing: **Product, Price, Place, and Promotion**.

## 📂 Dataset Information

The analysis utilizes two primary files:

* `marketing_data.csv`: The core dataset containing customer demographics, spending habits, channel preferences, and campaign responses.
* `Data Dictionary - Response to marketing campaigns.xlsx`: A reference file defining the variables within the dataset.

## 🎯 Objectives

As a data scientist, the primary objective is to conduct EDA and hypothesis testing to enhance the comprehension of the diverse factors influencing customer acquisition and purchasing behavior.

## 🛠️ Tech Stack & Requirements

The project is written in Python. Ensure you have the following libraries installed:

* `pandas` (Data manipulation)
* `numpy` (Numerical operations)
* `matplotlib` (Static visualizations)
* `seaborn` (Statistical data visualization)
* `scipy` (Hypothesis testing)

You can install the required packages using pip:

```bash
pip install pandas numpy matplotlib seaborn scipy

```

## 🚀 Steps Performed

1. **Data Importation & Verification:** Loaded data and verified formatting, specifically correcting string-based currency values and datetime formats (`Dt_Customer`).
2. **Data Cleaning & Imputation:** Consolidated redundant categorical variables (e.g., `Marital_Status`) and imputed missing `Income` values based on average income by education and marital status.
3. **Feature Engineering:** Derived new, high-value variables:
* `Total_Children`
* `Age` (Relative to 2021)
* `Total_Spending` (Sum of all product categories)
* `Total_Purchases` (Sum of all distribution channels)


4. **Outlier Treatment:** Generated boxplots and histograms to visualize distributions, subsequently capping extreme income outliers and filtering biologically improbable ages.
5. **Encoding:** Applied Ordinal Encoding to the `Education` feature and One-Hot Encoding to categorical fields like `Marital_Status` and `Country` to prepare for machine learning.
6. **Correlation Analysis:** Generated a heatmap to illustrate the relationships and multicollinearity between all numerical pairs.
7. **Hypothesis Testing:**
* Tested if older individuals lean toward traditional in-store shopping.
* Analyzed if customers with children favor online shopping due to time constraints.
* Investigated the potential cannibalization of in-store sales by alternative channels (Web/Catalog).
* Conducted a T-test to determine if the United States significantly outperforms the Rest of the World in purchase volume.


8. **Business Insights & Visualizations:** Analyzed top-performing products, campaign acceptance by age and geography, the impact of family size on total expenditure, and complaints segmented by education level.

## 💡 Key Insights

* **Product Performance:** Wine and Meat products are the overwhelming revenue drivers, while Fruits and Sweets lag significantly.
* **Demographic Spending:** Total household expenditure drops sharply as the number of children in the household increases. Childless households are the most lucrative demographic.
* **Omnichannel Engagement:** Web and catalog purchases correlate positively with in-store purchases, suggesting that high-value customers utilize multiple channels rather than cannibalizing physical store sales.

## 💻 How to Run

1. Clone this repository or download the project files.
2. Ensure both `marketing_data.csv` and the Python script/notebook are in the same directory.
3. Run the Jupyter Notebook (`marketing_campaign_analysis.ipynb`) cell-by-cell, or execute the Python script (`marketing_analysis.py`) via your terminal:
```bash
python marketing_analysis.py

