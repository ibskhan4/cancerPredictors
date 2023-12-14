# Predicting County-Level Cancer Incidence and Mortality Rate with Demographic Characteristics

## Contributors
- Tucker Boynton
- Chase Bookin
- Ibraheem Khan

---

### Overview

This project focuses on predicting cancer incidence and mortality rates at the county level using demographic indicators like per-capita income, unemployment rate, high-school dropout rate, disabled persons rate, minority share, poverty line percentage, and share of housing structures with at least 10 units. The study employs exploratory data analysis (EDA) to understand relationships between predictors and the target variables. Various machine learning models such as polynomial regression, LASSO regression, decision trees, random forests, bagging, and gradient boosting are utilized to predict rates and assess model performance.

### Data

Data sources include county-level cancer data and demographic statistics obtained from the Centers for Disease Control and Prevention. Observations missing all predictors (54) are excluded from the analysis, while instances with missing target variable data (70) are imputed using a discrete uniform distribution from 1-15.

### Model Overview

#### Polynomial Linear Regression
- Determines the best degree via cross-validation and assesses performance.

#### LASSO
- Implements regularization to improve model performance and selects alpha using cross-validation.

#### Decision Trees, Random Forests, and Bagging
- Identifies optimal tree depths and number of estimators through cross-validation.
- Evaluates performance compared to individual decision trees.

#### Gradient Boosting
- Employs gradient boosting with optimized parameters.

### Results Summary

#### Incidence
- Best-performing model: Bagging
- R-squared (best model): 0.429

#### Mortality
- Best-performing model: Random Forest
- R-squared (best model): 0.374

### Results

| Model | Test MSE | R-squared |
|-------|----------|-----------|
| **Incidence** | | |
| Polynomial (degree 1) | 10,996.431 | 0.394 |
| LASSO (alpha 0.1) | 11,264.117 | 0.379 |
| Decision Tree (depth 3) | 12,240.119 | 0.325 |
| Random Forest (depth 9) | 10,394.164 | 0.427 |
| Bagging (depth 9) | 10,367.975 | 0.429 |
| Boosting | 10,492.543 | 0.422 |
| **Mortality** | | |
| Polynomial (degree 1) | 3,087.628 | 0.343 |
| LASSO (alpha 0.01) | 3,085.608 | 0.343 |
| Decision Tree (depth 4) | 3,332.279 | 0.291 |
| Random Forest (depth 17) | 2,942.509 | 0.374 |
| Bagging (depth 17) | 3,038.686 | 0.353 |
| Boosting | 2,968.460 | 0.368 |


