Mani-Jafari

This project implemented a Gaussian Naive Bayes (GaussianNB) classifier to predict whether a breast tumor is benign or malignant based on numerical diagnostic features.

The dataset contained 569 observations and 33 columns. During the initial data inspection, no duplicate records were found. The `Unnamed: 32` column contained only missing values and was therefore excluded from the modeling process. The `id` column was also not considered a meaningful predictive feature.

The target variable, `diagnosis`, contained two classes:

* B (Benign): 357 observations
* M (Malignant): 212 observations

The dataset included 30 numerical diagnostic features describing characteristics such as radius, texture, perimeter, area, smoothness, compactness, concavity, symmetry, and fractal dimension.

After separating the features and target variable, the data was divided into training and testing sets. A Gaussian Naive Bayes classifier was then trained directly on the numerical features.

Model Performance:

* Test Accuracy: 95%
* Macro Average Precision: 0.95
* Macro Average Recall: 0.94
* Macro Average F1-Score: 0.94
* Weighted Average F1-Score: 0.95

Class-level performance:

* Benign (B): Precision = 0.95, Recall = 0.97, F1-Score = 0.96
* Malignant (M): Precision = 0.95, Recall = 0.90, F1-Score = 0.93

The model achieved an overall accuracy of approximately 95% on the unseen test set. The results show strong classification performance for both classes.

The model achieved a recall of 0.90 for the malignant class, meaning that most malignant cases in the test set were correctly identified. However, some malignant cases were classified as benign. In a medical classification context, this type of error is particularly important because failing to identify a malignant case can have serious consequences.

Overall, this project demonstrates that Gaussian Naive Bayes can provide strong performance for binary classification problems involving numerical features. Despite its relatively simple probabilistic approach and assumption about feature distributions, the model achieved a high level of predictive performance on this dataset.

However, the results should not be interpreted as clinical performance. The dataset is relatively small, and the model should be evaluated using additional validation techniques and independent data before being considered for any real-world medical application.

Key Steps:

1. Data loading and inspection
2. Dataset structure and statistical analysis
3. Duplicate and missing-value checking
4. Removal of irrelevant and empty columns
5. Target class distribution analysis
6. Feature-target separation
7. Train-test splitting
8. Gaussian Naive Bayes model training
9. Prediction on the test set
10. Evaluation using Precision, Recall, F1-Score, and Accuracy
11. Class-level performance analysis
12. Interpretation of classification errors

