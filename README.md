# MSCS_634_ProjectDeliverable_2
Deliverable 2 for Big Data and Data Mining project

## Summary
### Data Pre-processing
- This deliverable focuses on building and evaluating regression models to predict the final grade (G3) using the UCI Student Performance dataset. I continued from Deliverable 1 by adding new engineered features like `total_alc`, `high_absences`, and `had_failures`, and I created two different feature sets: one that includes prior grades (G1 and G2) and one that removes them to avoid any grade leakage.

### Model Training
- I trained Linear Regression, Ridge, and Lasso models and evaluated them using R^2, MSE, RMSE, and 5-fold cross-validation. The results were very straightforward. When I included G1 and G2, every model performed extremely well, reaching R^2 values around 0.85–0.88 with very low RMSE. That basically means the model can predict a student’s final grade within roughly one point, which shows how strongly prior grades drive final performance. When I removed G1 and G2, the accuracy dropped significantly, with R^2 around 0.15–0.20 and RMSE closer to 3, meaning the model had to rely on weaker behavioral and demographic predictors.

### Data Analysis
I inspected the coefficients from the Ridge and Lasso models using the stricter feature set. Features like planning to pursue higher education, attending school GP, parental education, study time, and even not being in a romantic relationship all showed positive influence on final performance. Overall, this deliverable helped me understand how different types of features contribute to prediction and how much more challenging the task becomes without access to prior academic history.
