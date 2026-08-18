Mani-Jafari

This project implemented a Decision Tree Classifier to predict the appropriate drug category based on several patient-related features.

The dataset contained 200 observations and 6 columns, including Age, Sex, Blood Pressure, Cholesterol Level, Sodium to Potassium Ratio, and Drug. During the initial data inspection, no duplicate records or missing values were found.

The target variable, Drug, contained five classes:

* Drug A: 23 observations

* Drug B: 16 observations

* Drug C: 16 observations

* Drug X: 54 observations

* Drug Y: 91 observations

During preprocessing, the categorical features Sex and Cholesterol Level were encoded numerically. The target values were also cleaned by removing the "drug" prefix from the original class labels.

Categorical features were converted into numerical representations using one-hot encoding. The dataset was then divided into training and testing sets using an 82/18 split. Stratified sampling was applied to preserve the class distribution between the training and testing sets.

A Decision Tree Classifier was trained using the Gini impurity criterion.

Model Performance:

* Test Accuracy: 100%

* Macro Average Precision: 1.00

* Macro Average Recall: 1.00

* Macro Average F1-Score: 1.00

* Weighted Average F1-Score: 1.00

Class-level performance:

* Class A: Precision = 1.00, Recall = 1.00, F1-Score = 1.00

* Class B: Precision = 1.00, Recall = 1.00, F1-Score = 1.00

* Class C: Precision = 1.00, Recall = 1.00, F1-Score = 1.00

* Class X: Precision = 1.00, Recall = 1.00, F1-Score = 1.00

* Class Y: Precision = 1.00, Recall = 1.00, F1-Score = 1.00

The Decision Tree achieved perfect classification performance on the test set, correctly predicting all 36 test observations. The confusion matrix confirms that there were no misclassified samples across any of the five drug classes.

A multiclass ROC curve was also generated using the predicted probabilities to provide an additional evaluation of the classifier's ability to distinguish between the different drug classes.

Finally, the trained Decision Tree was visualized using a tree plot, making the model's decision-making structure and feature-based splits easier to interpret.

Overall, this project demonstrates the effectiveness and interpretability of Decision Tree Classifiers for multiclass classification. The model achieved excellent performance on the available test set and provides a clear visual representation of the decision-making process.

However, the perfect 100% test accuracy should be interpreted with caution. The dataset is relatively small, and a single train-test split may not fully represent the model's generalization performance. Applying cross-validation and evaluating the model on an independent dataset would provide a more robust assessment of its real-world performance.

Key Steps:

1. Data loading and inspection

2. Exploratory Data Analysis (EDA)

3. Duplicate and missing-value checking

4. Categorical feature encoding

5. Target variable cleaning

6. One-hot encoding

7. Feature-target separation

8. Stratified train-test splitting

9. Decision Tree model training

10. Prediction on the test set

11. Classification Report analysis

12. Confusion Matrix analysis

13. Multiclass ROC Curve analysis

14. Decision Tree visualization
