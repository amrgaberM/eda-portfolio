
# Titanic - Exploratory Data Analysis

This repository contains a beginner-level exploratory data analysis (EDA) of the Titanic dataset from Kaggle.

## Objective
Understand the characteristics and patterns in the Titanic dataset to identify factors that influenced passenger survival.

## Dataset
- Source: [Kaggle Titanic Dataset](https://www.kaggle.com/c/titanic/data)
- The dataset includes demographic and travel information for passengers aboard the Titanic.

## Key Steps

1. **Data Loading and Inspection**
   - Reviewed dataset shape, column types, and basic structure.
   - Identified missing values and duplicate records.

2. **Data Cleaning**
   - Handled missing values in `Age` and `Embarked`.
   - Dropped the `Cabin` column due to excessive missing values.
   - Removed duplicate rows.

3. **Univariate Analysis**
   - Explored individual features using histograms, boxplots, and bar charts.
   - Identified skewed distributions and potential data quality issues.

4. **Bivariate Analysis**
   - Analyzed the relationship between features and the target variable `Survived`.
   - Focused on `Sex`, `Pclass`, `Age`, `Fare`, and `Embarked`.

5. **Outlier Detection**
   - Applied the IQR method to detect and handle outliers in `Fare` and `Age`.

6. **Key Insights**
   - Female passengers had significantly higher survival rates.
   - First-class passengers were more likely to survive than those in lower classes.
   - Children and passengers who paid higher fares had higher survival rates.
   - Traveling alone was associated with lower survival odds.

## Tools Used
- Python
- Pandas
- NumPy
- Seaborn
- Matplotlib
