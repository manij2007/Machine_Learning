Mani-Jafari

This project implemented a K-Nearest Neighbors (KNN) Classifier to predict whether a client would default on a loan based on financial and demographic features.

The dataset initially contained 2,000 observations and 6 columns. No duplicate records or missing values were found during the data inspection. The clientid column was removed because it does not provide meaningful predictive information. The final features used for classification were Income, Age, Loan, and LTI (Loan-to-Income ratio).

The target variable was imbalanced, with 1,717 non-default cases and 283 default cases. To preserve the original class distribution in both subsets, a stratified train-test split was used with 78% of the data for training and 22% for testing.

Since KNN is a distance-based algorithm, all numerical features were standardized using StandardScaler before training.

To determine the optimal number of neighbors, 10-fold cross-validation was performed for K values ranging from 1 to 99. The best performance was achieved with K = 8.

The final KNN model was trained using:

n_neighbors = 8

weights = 'uniform'

p = 2 (Euclidean distance)

Model Performance:

Test Accuracy: 98%

Precision (Class 0): 0.98

Recall (Class 0): 0.99

F1-Score (Class 0): 0.99

Precision (Class 1): 0.97

Recall (Class 1): 0.90

F1-Score (Class 1): 0.93

Macro Average F1-Score: 0.96

The model achieved an overall accuracy of approximately 98% on the unseen test set. The performance was strong for both classes, although the recall for the default class was slightly lower than for the non-default class. This means that while the model identifies most default cases correctly, a small portion of actual defaults are still classified as non-default.

The Confusion Matrix, Precision-Recall Curve, and ROC Curve were also used to further evaluate the classification performance and provide a more detailed understanding of the model's behavior.

Overall, this project demonstrates that K-Nearest Neighbors can achieve excellent classification performance when the features are appropriately scaled and the number of neighbors is selected through cross-validation.

However, because the target variable is imbalanced, accuracy alone should not be considered sufficient for evaluating the model. Metrics such as recall, precision, F1-score, and the ROC/Precision-Recall curves are particularly important when the goal is to correctly identify loan defaults.

Key Steps:

Data loading and inspection

Data quality checking

Removal of the identifier column

Target class distribution analysis

Feature-target separation

Stratified train-test splitting

Feature standardization using StandardScaler

K-value selection using 10-fold cross-validation

KNN model training

Prediction on the test set

Evaluation using Precision, Recall, F1-Score, and Accuracy

Confusion Matrix analysis

Precision-Recall Curve analysis

ROC Curve analysis
