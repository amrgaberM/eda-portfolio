# 🩺 US Health Insurance Charges: Deep Exploratory Analysis & Statistical Modeling

This notebook presents a comprehensive exploratory data analysis (EDA) and foundational statistical modeling on the **U.S. Health Insurance dataset**, aiming to understand the factors that drive variation in medical charges.

## 🔍 Objectives

- Identify patterns and distributions in demographic and medical variables
- Assess relationships between features and insurance charges
- Quantify the impact of smoking, age, and BMI
- Validate findings using statistical inference and simulation
- Prepare the data and insights for future predictive modeling

---

## 📊 1. Dataset Overview

- Source: `/content/insurance.csv`
- Observations: 1,338
- Features: `age`, `sex`, `bmi`, `children`, `smoker`, `region`, `charges`
- ✅ No missing values
- ⚠️ 1 duplicated row found

---

## 📈 2. Exploratory Data Analysis (EDA)

### 🧮 Numerical Features
- **Distributions:**
  - `age` and `bmi` are approximately normal
  - `charges` is heavily **right-skewed**
- **Outliers:**
  - Detected in `charges` using boxplots
- **Transformations:**
  - Log transformation (`log_charges`) reduces skewness
  - Skewness reduced from `1.52 → -0.09`, kurtosis from `1.61 → -0.64`

### 🧾 Categorical Features
- **`sex`**: ~50.5% male, 49.5% female
- **`smoker`**: ~20.5% smokers, 79.5% non-smokers
- **`region`**: Nearly uniform distribution

### 📉 Cumulative Distribution Functions (CDFs)
- ~53% of individuals pay < \$10,000 in charges
- Clear visual separation between smokers and non-smokers in charge distribution

---

## 🔗 3. Variable Relationships

### 🔹 Correlation Analysis
| Feature Pair         | Pearson r | Spearman ρ |
|----------------------|-----------|-------------|
| Age vs. Charges      | 0.299     | 0.534       |
| BMI vs. Charges      | 0.198     | 0.119       |
| Smoker vs. Charges   | 0.787     | 0.664       |
| Sex vs. Charges      | 0.057     | 0.010       |

- 🔥 **Smoking** shows the strongest positive correlation with `charges`
- 📉 Weak or no correlation for `sex`, `children`

### 🟦 Heatmap Summary
- Confirmed strong linear correlation between `smoker` and `charges`

---

## 📐 4. Distribution Fitting

- Attempted fitting **log-normal** and **Pareto** distributions on `charges`
- Log-normal fits best — confirmed by Q-Q plots and CDF comparison
- Different parameter estimates for smokers vs. non-smokers → distinct distributions

---

## 🧪 5. Statistical Inference

### 🔍 Mean Charges
- **Smokers**: \$32,050.23  
- **Non-Smokers**: \$8,434.27  
- **Difference**: \$23,615.96

### 🧪 Permutation Test
- **p-value**: 0.0000  
- ✅ Statistically significant difference in charges between smokers and non-smokers

---

## 📉 6. Linear Modeling (Age → Charges)

- **Model**: `charges = 257.72 × age + 3165.88`
- **R²**: 0.089 → Only 8.9% of variance explained
- **RMSE**: \$11,551.67
- **Residuals**: Heteroscedastic — error increases with age

---

## 🔁 7. Bootstrapping for Confidence Intervals

- 1,000-sample **bootstrap** on `charges`
- **95% CI for mean charges**: [\$12,638.69, \$13,919.70]

---

## 🧠 Key Takeaways

- **Smoking status** is the most influential factor for medical charges.
- **Age** and **BMI** have minor but noticeable effects.
- **Log transformation** improves charge distribution for modeling.
- Simple linear regression on `age` is inadequate for real-world prediction.
- Bootstrapping and permutation testing confirm statistical reliability of insights.

---

## 📦 Next Steps

- Build multivariate regression models incorporating:
  - `smoker`, `age`, `bmi`, `region`, and interaction terms
- Explore tree-based models and regularization
- Consider feature engineering for insurance risk scoring

---

## 📁 File Structure

- `deep_eda-US_Health_Insurance_Dataset.ipynb` – Main notebook
- `insurance.csv` – Input dataset

