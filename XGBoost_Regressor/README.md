Mani-Jafari

This project implemented an XGBoost Regressor to predict used car selling prices based on vehicle characteristics and market-related features.

The original dataset contained 301 observations and 9 columns. During data inspection, 2 duplicate records were identified and removed, resulting in 299 observations. 

No missing values were found.

The `Car_Name` feature was removed because it contains many unique categorical values and was not used as a predictive feature. The `Year` feature was transformed into 

`Age` to represent the age of each vehicle more directly.

Exploratory Data Analysis was performed using descriptive statistics, distributions, histograms, and a correlation heatmap. An extreme observation with a selling price 

above 30 was also removed during the data cleaning process.

For preprocessing, the categorical features `Seller_Type` and `Transmission` were encoded using LabelEncoder, while the remaining categorical features were converted 

using one-hot encoding.

The target variable was `Selling_Price`, and the dataset was divided into training and testing sets using an 80/20 split with a fixed random state.

An XGBoost Regressor with the `reg:squarederror` objective was used for prediction. RandomizedSearchCV with 5-fold cross-validation and 10 random parameter 

combinations was applied to search for an effective set of hyperparameters.

The best-performing configuration was:

* n_estimators = 118

* gamma = 0.0366

* learning_rate = 0.2779

* max_depth = 3

* subsample = 0.6143

Model Performance:

* MAE: 0.4231

* MSE: 0.4935

* RMSE: 0.7025

* R² Score: 0.9581

The model achieved an R² score of approximately 95.81%, indicating that the model explains a large proportion of the variation in used car selling prices within the 

test set.

The MAE of approximately 0.42 indicates that the model's predictions were, on average, relatively close to the actual selling prices. The RMSE of approximately 0.70 

also indicates that the prediction errors remained relatively low, although larger errors have a greater influence on this metric.

The Actual vs. Predicted plot shows that most predictions are relatively close to the ideal prediction line. Residual analysis was also performed to examine the 

distribution of prediction errors and provide additional insight into the model's behavior.

Overall, this project demonstrates the effectiveness of XGBoost for regression problems involving both numerical and categorical features. The combination of gradient 

boosting and hyperparameter optimization resulted in strong predictive performance on the available test data.

However, the model's performance is specific to the selected dataset and train-test split. Additional validation, such as repeated cross-validation or evaluation on an 

independent dataset, could provide a more reliable estimate of the model's generalization capability.

Key Steps:

1. Data loading and inspection

2. Duplicate and missing-value checking

3. Removal of the `Car_Name` feature

4. Transformation of `Year` into `Age`

5. Exploratory Data Analysis (EDA)

6. Outlier/data cleaning

7. Categorical feature encoding

8. One-hot encoding

9. Feature-target separation

10. Train-test splitting

11. XGBoost Regressor implementation

12. Hyperparameter optimization using RandomizedSearchCV

13. 5-fold cross-validation

14. Prediction on the test set

15. Evaluation using MAE, MSE, RMSE, and R²
16. Actual vs Predicted analysis

17. Residual analysis
