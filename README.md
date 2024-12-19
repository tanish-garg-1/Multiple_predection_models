# Multiple_predection_models

## Detailed result analysis

The performance of the models is evaluated based on three metrics: Mean Squared Error (MSE), Mean Absolute Error (MAE), and R² Score. Here's a detailed breakdown of the results:

1. Linear Regression
MSE: 0.00339
MAE: 0.04861
R² Score: 0.25108
Linear Regression provides a moderate fit for the data. While it has a relatively low MSE and MAE, the R² score indicates that only about 25% of the variance in the target variable is explained by the model.

2. Ridge Regression
MSE: 0.00339
MAE: 0.04861
R² Score: 0.25109
Ridge Regression performs almost identically to Linear Regression, as expected. The regularization parameter (alpha) does not seem to significantly impact the results for this dataset.

3. Lasso Regression
MSE: 0.00350
MAE: 0.04975
R² Score: 0.22747
Lasso Regression performs slightly worse than Linear Regression, with a marginally higher MSE and MAE and a reduced R² score. This suggests that the L1 regularization used by Lasso might not be effectively removing insignificant features.

4. Random Forest
MSE: 0.00362
MAE: 0.05035
R² Score: 0.20096
Random Forest provides a reasonable fit but performs slightly worse than the linear models. The MSE and MAE are higher, and the R² score indicates that it explains only about 20% of the variance.

5. Gradient Boosting
MSE: 0.00366
MAE: 0.05013
R² Score: 0.19112
Gradient Boosting performs similarly to Random Forest but slightly worse overall. It may require hyperparameter tuning (e.g., learning rate, depth) to improve performance.

6. AdaBoost
MSE: 0.00334
MAE: 0.04850
R² Score: 0.26151
AdaBoost outperforms most other models, achieving the highest R² score (26.15%). This indicates that boosting methods are better suited for this dataset, as they iteratively improve weak learners.

7. Extra Trees
MSE: 0.00365
MAE: 0.05038
R² Score: 0.19314
Extra Trees performs similarly to Random Forest, but it slightly underperforms AdaBoost and Gradient Boosting. Its higher MSE and lower R² indicate it explains less variance in the target variable.

8. Support Vector Regressor (SVR)
MSE: 0.00378
MAE: 0.05183
R² Score: 0.16572
SVR performs worse than most other models. Its relatively high MSE and low R² score indicate that it does not generalize well for this dataset. Kernel or hyperparameter tuning may improve its performance.

9. K-Nearest Neighbors (KNN)
MSE: 0.00489
MAE: 0.05784
R² Score: -0.07930
KNN performs poorly on this dataset, with a high MSE and negative R² score, indicating that the model fails to explain the variance in the target variable and performs worse than a simple mean baseline.

10. Decision Tree
MSE: 0.00775
MAE: 0.07313
R² Score: -0.71125
Decision Tree performs the worst among all models, with a very high MSE and a significantly negative R² score. This indicates severe overfitting on the training data, as the model does not generalize well.


Visualization of Results
A bar chart comparing the R² scores of the models is provided to visually illustrate performance differences.

AdaBoost is at the top, followed closely by Linear Regression and Ridge Regression.
Decision Tree and KNN show the poorest results.
