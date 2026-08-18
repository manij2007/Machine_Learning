Mani-Jafari

This project implemented a Random Forest Classifier to predict the species of penguins based on their physical characteristics and other categorical features.

The dataset initially contained 344 observations and 7 columns. No duplicate records were found. However, several missing values were present, so rows containing missing values were removed, resulting in 334 observations.

During data preprocessing, an invalid value in the `sex` feature was identified and corrected. The categorical `sex` feature was encoded using LabelEncoder, while the remaining categorical features were converted into numerical form using one-hot encoding.

The target variable was `species`, containing three classes:

* Adelie: 146 observations

* Gentoo: 120 observations

* Chinstrap: 68 observations

The dataset was divided into training and testing sets using an 80/20 split.

A Random Forest Classifier was trained using:

* n_estimators = 10

* max_features = "sqrt"

* random_state = 101

Model Performance:

* Test Accuracy: 97%

* Macro Average Precision: 0.97

* Macro Average Recall: 0.97

* Macro Average F1-Score: 0.97

Class-level performance:

* Adelie: Precision = 0.97, Recall = 0.97, F1-Score = 0.97

* Chinstrap: Precision = 0.95, Recall = 0.95, F1-Score = 0.95

* Gentoo: Precision = 1.00, Recall = 1.00, F1-Score = 1.00

The model achieved an overall accuracy of approximately 97% on the unseen test set. The results show strong and balanced classification performance across all three penguin species. Gentoo was classified perfectly, while only a small number of observations from Adelie and Chinstrap were misclassified.

A confusion matrix was used to analyze the classification errors, and a multiclass ROC curve was generated using the predicted probabilities to provide an additional evaluation of the model's classification performance.

Overall, this project demonstrates that Random Forest can provide excellent performance for multiclass classification problems. Its ability to combine multiple decision trees allows it to capture complex relationships between the features without requiring extensive feature transformations.

However, the dataset is relatively small, so the reported test performance may vary with a different train-test split. Using cross-validation and optimizing the Random Forest hyperparameters could provide a more robust estimate of the model's generalization performance.

Key Steps:

1. Data loading and inspection

2. Duplicate and missing-value checking

3. Data cleaning and preprocessing

4. Correction of invalid categorical data

5. Categorical feature encoding

6. Feature-target separation

7. Train-test splitting

8. Random Forest model training

9. Prediction on the test set

10. Evaluation using Precision, Recall, F1-Score, and Accuracy
11. Confusion Matrix analysis

12. Multiclass ROC Curve analysis
