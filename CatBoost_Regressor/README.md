Mani-Jafari

The CatBoost Regressor was applied to predict house sale prices using a dataset containing 1,460 observations and 81 features, including both numerical and categorical variables. The preprocessing stage addressed missing values using appropriate strategies such as median, mode, and meaningful categorical labels. Several potential outliers were also removed based on relationships between important housing features and the target variable.

The dataset was divided into training and testing sets using a 79/21 split. CatBoost was selected because it can handle categorical features directly without requiring conventional one-hot encoding. The final model used 500 iterations, a learning rate of 0.05, a tree depth of 6, RMSE as the loss function, and a fixed random seed of 101.

The model achieved an **R² score of 0.9120**, indicating that it explains approximately 91.2% of the variance in house sale prices on the test set. The model also achieved an **MAE of approximately $14,627.87** and an **RMSE of approximately $21,723.88**, demonstrating relatively accurate predictions while still showing some larger prediction errors.

Overall, the CatBoost Regressor performed strongly on this dataset and proved to be an effective choice for a regression problem containing a large number of categorical and numerical features. The high R² score and relatively low prediction errors indicate that the model successfully captured the major relationships between housing characteristics and sale prices. Further improvements could potentially be achieved through additional hyperparameter tuning, cross-validation, feature engineering, and more systematic outlier analysis.
