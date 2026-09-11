Mani-Jafari

The K-Neighbors Regressor was applied to the Boston housing dataset to predict the `MEDV` target variable based on 13 numerical features. The dataset contained **506 observations and 14 columns**, with **no missing values and no duplicate records**.

During the exploratory data analysis, the distributions of the variables and the correlation structure between features were examined. The `MEDV` variable was selected as the target, while the remaining 13 features were used as predictors.

Since K-Nearest Neighbors is a distance-based algorithm, **StandardScaler** was applied within a Pipeline to standardize the features before modeling. A **GridSearchCV with 10-fold cross-validation** was then used to find the optimal number of neighbors, testing values from 1 to 11.

The best-performing configuration selected **7 neighbors**. The final model used uniform weights, Euclidean distance through the Minkowski metric (`p=2`), and standardized input features.

### Key Performance Metrics

* **Best `n_neighbors`:** 7
* **MAE:** 3.5315
* **MSE:** 26.3080
* **RMSE:** 5.1291
* **R² Score:** 0.7688
* **Training/Test Split:** 78% / 22%
* **Cross-Validation:** 10-fold

The model achieved an **R² score of 0.7688**, meaning that approximately **76.9% of the variance in `MEDV`** was explained by the model on the test set. The **RMSE of 5.1291** indicates that the typical prediction error is around 5.13 units of the target variable.

Overall, the K-Neighbors Regressor provided a **reasonably strong regression performance** on the dataset. The combination of feature scaling and cross-validation-based hyperparameter tuning helped establish an appropriate neighborhood size and provided a more reliable modeling workflow.
