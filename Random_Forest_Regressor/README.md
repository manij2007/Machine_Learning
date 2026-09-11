Mani-Jafari

The Random Forest Regressor was applied to the **Bike Sharing dataset** to predict the `cnt` target variable, representing the total number of bike rentals.

The dataset initially contained **730 observations and 16 columns**. During feature engineering, the `dteday` column was converted to a datetime format, and two new features, `day` and `year`, were extracted. The columns `dteday`, `yr`, and `instant` were then removed from the dataset. After preprocessing, the dataset contained **15 columns** with **no missing values or duplicate records**.

Exploratory Data Analysis was performed to examine the distributions and relationships between the variables. The correlation analysis showed a particularly strong relationship between `registered` and the target `cnt`, with a correlation of **0.9454**, while `casual` also showed a strong correlation of **0.6721** with the target.

The final model was a **RandomForestRegressor** using **100 trees**, the default squared-error criterion, unrestricted tree depth, bootstrap sampling, and `random_state=101`.

### Key Performance Metrics

* **MAE:** 82.2286
* **MSE:** 15,452.1955
* **RMSE:** 124.3069
* **R² Score:** 0.9961
* **Total Samples:** 730
* **Features After Preprocessing:** 15
* **Number of Trees:** 100
* **Random State:** 101
* **Missing Values:** 0
* **Duplicate Records:** 0

The model achieved an **R² score of 0.9961**, meaning that approximately **99.61% of the variance in the target variable was explained by the model on the test set**. The RMSE was **124.31**, while the MAE was approximately **82.23**, indicating very accurate predictions relative to the scale of the target variable.

Overall, the Random Forest Regressor demonstrated **exceptionally strong predictive performance** on this dataset. However, an important consideration is that `registered` and `casual` are components of the total `cnt` value. Therefore, using these features to predict `cnt` can introduce **target leakage or feature leakage** in a real-world prediction scenario and can partly explain the extremely high R² score.

For a more realistic forecasting setup, the model should be evaluated without features that are directly derived from the target, followed by additional validation using cross-validation or a time-based train/test split.
