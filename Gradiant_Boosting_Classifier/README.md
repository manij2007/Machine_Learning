Mani-Jafari

This project implemented a Gradient Boosting Classifier to classify mushrooms as either edible or poisonous based on their physical characteristics.

The dataset contained 8,124 observations and 23 columns. During the initial data inspection, no duplicate records or missing values were found. The `veil-type` feature 

was removed because it contained only a single unique value and therefore provided no useful information for classification.

The target variable, `class`, contained two categories:

* Edible (e)

* Poisonous (p)

The dataset was converted into numerical form using one-hot encoding. The target variable was separated from the input features, and the data was divided into training 

and testing sets using a 75/25 split.

A Gradient Boosting Classifier was used for the classification task. RandomizedSearchCV with 5-fold cross-validation was applied to search for an effective combination 

of model hyperparameters.

The best-performing configuration was:

* n_estimators = 50

* max_depth = 4

* learning_rate = 0.05

Model Performance:

* Test Accuracy: 100%

* Precision (Edible): 1.00

* Recall (Edible): 1.00

* F1-Score (Edible): 1.00

* Precision (Poisonous): 1.00

* Recall (Poisonous): 1.00

* F1-Score (Poisonous): 1.00

* Macro Average F1-Score: 1.00

The model achieved 100% accuracy on the test set, correctly classifying all 2,031 test observations. Both edible and poisonous mushrooms were classified perfectly, 

with no false positives or false negatives in the test set.

The Confusion Matrix confirms that there were no classification errors. The Precision-Recall Curve and ROC Curve were also generated to provide additional evaluation 

of the classifier's performance.

Overall, this project demonstrates the strong capability of Gradient Boosting for binary classification problems involving categorical features. The combination of 

multiple weak learners allows Gradient Boosting to progressively improve its predictions and capture complex relationships within the data.

However, the perfect test performance should be interpreted with caution. Although cross-validation was used during hyperparameter optimization, achieving 100% 

accuracy on a single test split does not guarantee perfect performance on completely unseen real-world data. Further evaluation using independent datasets and 

additional validation techniques would provide a stronger assessment of the model's generalization capability.

Key Steps:

1. Data loading and inspection

2. Exploratory Data Analysis (EDA)

3. Duplicate and missing-value checking

4. Removal of the constant `veil-type` feature

5. Target variable analysis

6. One-hot encoding of categorical features

7. Feature-target separation

8. Train-test splitting

9. Gradient Boosting Classifier implementation

10. Hyperparameter optimization using RandomizedSearchCV

11. 5-fold cross-validation

12. Model prediction

13. Classification Report analysis

14. Confusion Matrix analysis

15. Precision-Recall Curve analysis

16. ROC Curve analysis
