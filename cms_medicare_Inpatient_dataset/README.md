# Medicare Inpatient Hospital Payment Analysis

## Overview

This repository contains a comprehensive analysis of Medicare Inpatient Hospital payment data, focusing on Average Total Payment patterns, distributions, and key relationships that influence healthcare costs. The analysis provides insights into payment variations across procedures, providers, and geographic regions.

## Dataset Description

The analysis is based on Medicare Inpatient Hospital payment data, examining various financial and operational metrics including:

- **Average Total Payment**: Primary target variable representing total payment amounts
- **Average Medicare Payment**: Medicare's portion of the total payment
- **Average Submitted Charge**: Hospital's submitted charges before adjustments
- **Total Discharges**: Volume of patient discharges
- **RUCA Code**: Rural-Urban Commuting Area classification
- **Geographic Information**: State-level and regional data
- **Procedure Categories**: Classification of medical procedures and treatments

## Key Findings

### Financial Characteristics
- **Wide Payment Range**: Payments span from minimum to maximum values with significant variation
- **High Variability**: Coefficient of variation exceeding industry norms indicates substantial cost differences
- **Right-Skewed Distribution**: Most payments cluster at lower amounts with a long tail of high-cost cases

### Distribution Properties
- **Non-Normal Distribution**: Statistical tests confirm significant deviation from normal distribution
- **Heavy-Tailed**: Higher frequency of extreme values compared to normal distribution
- **Outlier Presence**: Notable percentage of cases with unusually high payment amounts

### Relationship Analysis
- **Strong Positive Correlations**:
  - Average Medicare Payment (very strong relationship)
  - Average Submitted Charge (strong relationship with non-linear characteristics)
- **Weak Correlations**:
  - Total Discharges (slight negative correlation)
  - RUCA Code (weak negative correlation with rural areas)

## Analysis Components

### 1. Descriptive Statistics
- Central tendency measures (mean, median, mode)
- Variability assessment (standard deviation, coefficient of variation)
- Distribution shape analysis (skewness, kurtosis)

### 2. Outlier Detection
- Multiple detection methods (IQR, Modified Z-Score)
- Percentage identification and characterization
- Impact assessment on overall analysis

### 3. Correlation Analysis
- Pearson correlation matrix
- Relationship strength interpretation
- Visual scatter plot analysis

### 4. Segmentation Analysis
- Payment tier categorization
- High-cost case identification
- Geographic variation assessment
- Procedure category breakdown

## Methodology

### Statistical Tests Applied
- **Normality Tests**: Jarque-Bera, D'Agostino, Shapiro-Wilk
- **Outlier Detection**: Interquartile Range (IQR), Modified Z-Score methods
- **Correlation Analysis**: Pearson correlation coefficients

### Data Processing
- Distribution analysis and transformation considerations
- Outlier treatment strategies
- Segmentation approaches for deeper insights

## Visualizations

The analysis includes comprehensive visualizations:
- Distribution histograms and box plots
- Correlation heatmaps
- Scatter plots for relationship analysis
- Geographic payment variation maps
- Procedure category comparisons
- Payment segment breakdowns

## Recommendations

### Immediate Actions
1. **High-Payment Case Investigation**: Deep dive into top 5% payment cases
2. **Procedure Category Analysis**: Detailed cost analysis by medical procedure type
3. **Geographic Factor Study**: Regional cost driver identification

### Advanced Analysis
1. **Predictive Modeling**: Robust regression techniques for skewed data
2. **Submitted Charge Analysis**: Payment vs. charge discrepancy investigation
3. **Volume-Cost Relationship**: Economics of scale analysis



## Future Work

- **Longitudinal Analysis**: Time-series payment trend analysis
- **Patient Demographics**: Integration of demographic factors
- **Quality Metrics**: Correlation with patient outcomes
- **Predictive Modeling**: Advanced machine learning approaches
- **Cost-Effectiveness**: Analysis of payment efficiency



*This analysis provides a foundation for understanding Medicare payment patterns and can be extended for more specific research questions or policy applications.*
