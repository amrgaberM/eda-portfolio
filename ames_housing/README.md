# Ames Housing - Exploratory Data Analysis (EDA)

This repository presents a structured exploratory data analysis (EDA) of the [Ames Housing Dataset](https://www.kaggle.com/datasets/prevek18/ames-housing-dataset). This is a **large and rich dataset** with 2,930 observations and 81 features, posing **real-world challenges** such as missing data, high cardinality, multicollinearity, and outliers.

## Dataset Overview
- **Observations:** 2,930  
- **Features:** 81 (38 numeric, 43 categorical)  
- **Source:** Ames, Iowa housing data compiled by Dean De Cock  
- **Link:** [Kaggle Dataset](https://www.kaggle.com/datasets/prevek18/ames-housing-dataset)  

## Key Insights
- Substantial missing data in features like `Alley`, `Pool QC`, `Fence`, and others  
- Target variable `SalePrice` is right-skewed, with outliers > \$500,000  
- Strong predictors of `SalePrice`: `Overall Qual`, `Gr Liv Area`, `Total Bsmt SF`, `Garage Area`  
- `Neighborhood`, `Bldg Type`, and `House Style` show statistically significant price variation  
- High correlation and multicollinearity in numeric features (e.g., `Gr Liv Area`, `TotRms AbvGrd`)  

## Data Cleaning Summary
- Dropped columns with excessive missing data  
- Imputed remaining missing values using median (numeric) or mode (categorical)  
- Removed duplicates  
- Treated skewed features and investigated outliers  

## Recommendations
- Apply **log transformation** to skewed features  
- Use **categorical encoding**: One-Hot for nominal, Ordinal for ordered features  
- Engineer new features (e.g., total square footage, interaction terms)  
- Build predictive models (Linear Regression, Random Forest, Gradient Boosting)  
- Evaluate using **cross-validation**, **R²**, and **RMSE**  
- Consider feature selection to reduce dimensionality  

## Deliverables
-  Jupyter notebooks with full EDA workflow  
-  Visualizations for distributions, correlations, and trends  
- Executive summary with key findings and modeling strategy  



