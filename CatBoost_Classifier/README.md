Mani-Jafari

The CatBoost Classifier was used to predict the `Diabetes_Risk` level using a dataset containing demographic, physiological, lifestyle, and health-related features. The original dataset contained 50,000 records and 41 columns. After removing rows with missing values, 32,679 records remained. The `Patient_ID` column was removed because it does not provide meaningful predictive information.

The target variable contained three classes: **High, Moderate, and Low**. The data was split into training and testing sets using a 22% test size with stratification to preserve the class distribution.

CatBoost was selected because it can handle categorical features directly. The final model used **500 iterations**, a **learning rate of 0.05**, and a **tree depth of 7**, with the `MultiClass` loss function.

The model achieved **100% accuracy**, with **1.00 precision, recall, and F1-score for all three classes** on the test set. The confusion matrix also confirms the perfect classification performance.

Overall, CatBoost demonstrated excellent performance on this classification task and successfully learned the patterns within the dataset. However, because the model achieved perfect performance, further investigation into potential data leakage and highly predictive features would be important before considering the model fully reliable for real-world applications. Cross-validation and testing on an independent dataset could provide additional evidence of its generalization ability.
