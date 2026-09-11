Mani-Jafari

The LightGBM Classifier was applied to the Diabetes Risk dataset to predict the `Diabetes_Risk` target variable across three classes: **High, Moderate, and Low**.

The dataset contained **50,000 observations and 42 columns**. During the exploratory data analysis, no duplicate records were found. Several numerical and categorical features contained missing values, which were handled using median imputation for numerical variables and mode imputation for categorical variables. The `Patient_ID` column was removed, and categorical features were transformed using label encoding and one-hot encoding.

The data was divided into training and testing sets using an **80/20 stratified split**, resulting in **40,000 training samples and 10,000 test samples**. The final LightGBM model was configured with **110 estimators**, a **learning rate of 0.15**, a **subsample ratio of 0.4**, and a fixed `random_state` of 101.

### Key Performance Metrics

* **Accuracy:** 1.00
* **Macro Precision:** 1.00
* **Macro Recall:** 1.00
* **Macro F1-Score:** 1.00
* **Weighted F1-Score:** 1.00
* **Test Samples:** 10,000
* **Training Samples:** 40,000
* **Number of Features Used:** 89

The model achieved **perfect classification performance on the test set**, with precision, recall, and F1-score of **1.00 for all three classes**. The confusion matrix also confirms that the test samples were classified without observed errors.

Overall, the LightGBM Classifier demonstrated an **exceptionally strong performance** on this dataset. However, because the model achieved perfect scores, further validation using cross-validation and an independent dataset is recommended. It is also important to investigate potential **data leakage or target-derived features**, particularly when features may be directly or indirectly related to the construction of the `Diabetes_Risk` label.

Despite this consideration, the implemented workflow successfully handled mixed feature types, missing values, categorical encoding, stratified splitting, model training, and multiclass evaluation using LightGBM.
