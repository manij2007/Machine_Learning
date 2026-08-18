Mani-Jafari

This project implemented Polynomial Regression to predict product sales based on advertising expenditure across TV, radio, and newspaper channels.
The dataset contained 200 observations and 4 numerical columns. During the initial data inspection, no duplicate records or missing values were found, and all features were already stored in numerical form.

Exploratory Data Analysis was performed to understand the distributions and relationships between the advertising features and the target variable, Sales. Correlation analysis and scatter plots were also used to examine the relationships between advertising spending and sales.

To capture potential nonlinear relationships, Polynomial Features with degree 2 were generated. The resulting features were standardized using StandardScaler, and the data was divided into training and testing sets using an 80/20 split.

A Linear Regression model was then trained on the transformed polynomial features.

Model Performance:

MAE: 0.4431

MSE: 0.3375

RMSE: 0.5809

R² Score: 0.9886

The model achieved an R² score of approximately 98.86%, indicating that the polynomial model explains a very large proportion of the variation in Sales within this dataset. The low MAE and RMSE also show that the predicted sales values are generally very close to the actual values.

The Actual vs. Predicted plot shows that most predictions are closely aligned with the ideal prediction line. Residual analysis also provides an additional view of the model's prediction errors and helps evaluate how the model behaves on unseen data.

Overall, this project demonstrates how Polynomial Regression can extend a linear regression model by introducing nonlinear relationships between features and the target variable. In this dataset, the degree-2 polynomial model achieved excellent predictive performance.

However, the results are specific to the available dataset and train-test split. Additional validation, such as cross-validation and testing on independent data, would be useful to evaluate the model's generalization capability more reliably.

Key Steps:

Data loading and inspection

Exploratory Data Analysis

Data quality checking

Feature-target separation

Polynomial feature generation (degree 2)

Train-test splitting

Feature standardization

Polynomial Regression model training

Model evaluation using MAE, MSE, RMSE, and R²

Actual vs Predicted analysis

Residual analysis
