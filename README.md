# Predicting County-Level Cancer Incidence and Mortality Rate with Demographic Characteristics
## Project Overview:

This project aims to predict county-level cancer incidence and mortality rates (per 100,000 people) using demographic characteristics. We explore the relationship between various factors like per-capita income, unemployment rate, education level, and minority share with cancer rates. We then compare the performance of several machine learning models, including polynomial regression, LASSO, decision trees, random forests, bagging, and gradient boosting, in predicting the target variables.

## Data and Methodology:

### Data:
* County-level cancer data from the Centers for Disease Control and Prevention (CDC)
* Demographic summary statistics from the CDC
* 54 observations dropped due to missing predictors
* 70 observations with missing target variables imputed using a discrete uniform distribution
### Models:
*Polynomial regression with hyperparameter tuning (degree)
*LASSO regression with hyperparameter tuning (alpha)
*Decision trees with hyperparameter tuning (depth)
*Random forests with hyperparameter tuning (depth, number of trees)
*Bagging (bootstrap aggregation) using decision trees
*Gradient boosting regression with hyperparameter tuning (learning rate)
Results:

Incidence:
Bagging model with depth 9 and 8 bootstraps performs best (test MSE: 10270.583, R-squared: 0.434)
Random forest with depth 9 performs second best
Gradient boosting and polynomial regression follow
Mortality:
Random forest with depth 17 performs best (test MSE: 2942.509, R-squared: 0.374)
Gradient boosting and bagging follow
Polynomial regression and LASSO perform least well
Key Takeaways:

Ensemble methods like bagging and random forests outperformed single decision trees and other models for both incidence and mortality prediction.
Demographic factors like per-capita income, unemployment rate, and education level play a role in cancer rates, though the relationships are complex.
Future Work:

Explore additional features like geographic and environmental factors.
Implement more advanced models like deep learning.
Investigate the reasons behind the observed relationships between demographics and cancer rates.
