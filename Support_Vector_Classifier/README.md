Mani-Jafari

This project implemented a Support Vector Classifier (SVC) to classify iris flowers into three different species: Setosa, Versicolor, and Virginica.

The dataset initially contained 150 observations and 5 columns. During data preprocessing, 3 duplicate records were identified and removed, resulting in 147 

observations. No missing values were found in the dataset.

Exploratory Data Analysis (EDA) was performed using descriptive statistics, histograms, scatter plots, and a correlation heatmap to understand the relationships 

between the numerical features and the target variable.

The four numerical features used for classification were:

* Sepal Length

* Sepal Width

* Petal Length

* Petal Width

The data was divided into training and testing sets using an 80/20 split. Since SVC can be sensitive to feature scale, StandardScaler was applied within a Pipeline 

before training the model.

GridSearchCV with 5-fold cross-validation was used to find the best SVC configuration. The best parameters were:

* C = 1.0

* Kernel = linear

* Gamma = scale

Model Performance:

* Test Accuracy: 93%

* Macro Average Precision: 0.94

* Macro Average Recall: 0.94

* Macro Average F1-Score: 0.94

Class-level performance:

* Setosa: Precision = 1.00, Recall = 1.00, F1-Score = 1.00

* Versicolor: Precision = 0.92, Recall = 0.92, F1-Score = 0.92

* Virginica: Precision = 0.90, Recall = 0.90, F1-Score = 0.90

The model achieved an overall accuracy of approximately 93% on the unseen test data. Setosa was classified perfectly, while most of the remaining classification errors 

occurred between Versicolor and Virginica, which have more similar characteristics.

A confusion matrix was used to examine the classification errors in more detail, and a multiclass ROC curve was generated using the predicted probabilities to further 

evaluate the model's classification performance.

Overall, this project demonstrates that Support Vector Classification can provide strong performance for multiclass classification problems, particularly when the 

features are properly scaled and the model hyperparameters are optimized using cross-validation.

However, because the Iris dataset is relatively small, the final performance should be interpreted with some caution. Testing the model on additional independent data 

or using repeated cross-validation would provide a more robust estimate of its generalization performance.

Key Steps:

1. Data loading and inspection

2. Duplicate removal

3. Missing-value checking

4. Exploratory Data Analysis (EDA)

5. Feature-target separation

6. Train-test splitting

7. Feature standardization using StandardScaler

8. SVC Pipeline creation

9. Hyperparameter optimization using GridSearchCV

10. 5-fold cross-validation

11. Model prediction

12. Classification Report analysis
13. Confusion Matrix analysis

14. Multiclass ROC Curve analysis
