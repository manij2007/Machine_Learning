Mani-Jafari

This project implemented a Support Vector Regressor (SVR) to predict the compressive strength of concrete based on its material composition and fresh concrete properties.

The dataset contained 103 observations and 10 numerical features. The input features included Cement, Slag, Fly Ash, Water, Superplasticizer (SP), Coarse Aggregate, Fine Aggregate, Slump, and Flow. The target variable was Compressive Strength.

During the initial data inspection, no duplicate records or missing values were found. All features and the target variable were numerical and stored as floating-point values.

Exploratory Data Analysis (EDA) was performed using descriptive statistics, feature distributions, correlation analysis, and scatter plots to investigate the relationships between the input variables and compressive strength.

The dataset was divided into training and testing sets using a fixed test size of 18 observations and a random state of 101.

Because Support Vector Regression is sensitive to the scale of the input features, StandardScaler was applied as part of a Pipeline. This ensured that feature scaling was performed consistently during both training and prediction.

GridSearchCV with 5-fold cross-validation was used to search for the best SVR configuration. The model was optimized using negative mean squared error as the scoring metric.

The best-performing configuration was:

* Kernel = linear
* C = 10.0
* Gamma = scale
* Degree = 2
* Epsilon = 2

Model Performance:

* MAE: 1.6930
* MSE: 4.7890
* RMSE: 2.1884
* R² Score: 0.9329

The model achieved an R² score of approximately 93.29%, indicating that the SVR model explains a large proportion of the variation in concrete compressive strength within the test set.

The Mean Absolute Error of approximately 1.69 indicates that the model's predictions differ from the actual compressive strength values by about 1.69 units on average. The RMSE of approximately 2.19 indicates that larger prediction errors have a somewhat greater impact on the overall error measurement.

The Actual vs. Predicted plot shows a strong agreement between the predicted and actual compressive strength values, while the residual distribution provides additional insight into the model's prediction errors.

Overall, this project demonstrates that Support Vector Regression can be an effective approach for predicting continuous engineering properties when the input features have been properly scaled and the model hyperparameters are optimized using cross-validation.

The use of a Pipeline combined with GridSearchCV provided a structured and reliable workflow for preprocessing, model selection, and training.

However, the dataset is relatively small, with only 103 observations, and the test set contains just 18 observations. Therefore, the reported performance may be sensitive to the particular train-test split. Using repeated cross-validation or evaluating the model on an independent dataset would provide a more robust estimate of its generalization performance.

Key Steps:

1. Data loading and inspection
2. Dataset structure and statistical analysis
3. Duplicate and missing-value checking
4. Exploratory Data Analysis (EDA)
5. Correlation and relationship analysis
6. Feature-target separation
7. Train-test splitting
8. Feature standardization using StandardScaler
9. SVR Pipeline creation
10. Hyperparameter optimization using GridSearchCV
11. 5-fold cross-validation
12. Model prediction
13. Evaluation using MAE, MSE, RMSE, and R²
14. Actual vs. Predicted analysis
15. Residual analysis

