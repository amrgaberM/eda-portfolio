# Chronic Kidney Disease (CKD) – Exploratory Data Analysis

## Project Overview

This repository contains an in-depth exploratory data analysis (EDA) of a Chronic Kidney Disease (CKD) dataset. The primary objective is to investigate the underlying data structure, assess data quality, uncover feature-target relationships, and prepare the dataset for predictive modeling. The dataset includes both clinical and demographic variables relevant to the diagnosis and progression of CKD.

---

## Repository Structure

- `ckd_eda.ipynb`: Jupyter notebook containing the full EDA workflow, including preprocessing, statistical summaries, visualizations, and interpretations.
- `data/`: Directory for storing the input dataset.
- `README.md`: Project documentation.

---

## Dataset Summary

- **Number of Observations:** 400  
- **Number of Features:** 26 (after removal of the identifier column)  
- **Target Variable:** `class` (converted to binary `class_numerical`: 1 = CKD, 0 = not CKD)

The dataset includes variables such as age, blood pressure, hemoglobin levels, specific gravity, albumin, serum creatinine, red and white blood cell counts, and other clinical measurements.

---

## Key Findings

### Data Quality and Preprocessing

- Missing values were found in several key features, particularly in laboratory results.
- Features with more than 20% missing data (e.g., red blood cell count, sodium, potassium) were imputed using median values for numeric features and mode for categorical variables.
- Inconsistent categorical values were cleaned (e.g., extra spaces or typographical differences).
- The target variable `class` was encoded numerically for compatibility with analytical tools.
- No duplicate entries were detected.

### Univariate Analysis

- Distributions of numerical features were analyzed through histograms, KDE plots, and summary statistics.
- Skewness and kurtosis calculations highlighted the presence of non-normal and heavy-tailed distributions.
- CDF and quantile analyses offered insights into data spread and thresholds for key variables such as hemoglobin and serum creatinine.

### Multivariate Analysis

- Correlation analysis identified strong linear relationships between certain variables, notably:
  - `specific_gravity` and `class_numerical`: -0.73
  - `hemoglobin` and `class_numerical`: -0.77
  - `packed_cell_volume` and `hemoglobin`: 0.90
- Visualizations including box plots and scatter plots revealed clear separations between CKD and non-CKD cases for selected features.
- CDF plots stratified by CKD class showed significant distributional shifts in critical biomarkers.

### Outlier Analysis

- Outliers were detected using both visual (box plots) and statistical (IQR method) approaches.
- Variables such as `serum_creatinine` and `red_blood_cell_count` exhibited significant outliers that may influence modeling results.

---

## Recommendations

1. **Handle Remaining Missing Data:** Evaluate imputation strategies beyond median/mode, such as KNN imputation or multiple imputation, depending on downstream modeling needs.
2. **Address Outliers:** Investigate extreme values for clinical plausibility. Apply robust scaling or transformations (e.g., log) where appropriate.
3. **Feature Engineering:** Derive interaction terms or polynomial features for variables with strong associations to CKD.
4. **Categorical Interaction Analysis:** Perform chi-squared tests or stratified visualizations to explore relationships between categorical variables and CKD status.
5. **Model Readiness:** Data is now suitable for binary classification models. Recommend further steps such as train/test splitting, standardization, and evaluation of multicollinearity among features.

---

## Next Steps

This EDA establishes a reliable foundation for building CKD prediction models. The cleaned and preprocessed dataset is ready for supervised learning tasks, including baseline logistic regression, tree-based classifiers, and ensemble models.

