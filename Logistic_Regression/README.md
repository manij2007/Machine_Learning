Mani-Jafari

This project implemented a Logistic Regression model to predict a binary target variable based on two main features: Age and Physical Score.

The original dataset contained 5,000 observations. During data preprocessing and exploratory data analysis, duplicate records and invalid or suspicious observations were identified and removed, resulting in a final dataset of 3,530 observations.

The selected features were standardized using StandardScaler, and Logistic Regression with L2 regularization was used as the classification algorithm. A Pipeline was implemented to combine preprocessing and model training, while GridSearchCV with 5-fold cross-validation was used to select the best model configuration.

The best-performing model used the LBFGS solver.

Model Performance:

Test Accuracy: 92%

Precision (Class 0): 0.93

Recall (Class 0): 0.90

F1-Score (Class 0): 0.91

Precision (Class 1): 0.91

Recall (Class 1): 0.93

F1-Score (Class 1): 0.92

The model achieved an overall accuracy of approximately 92% on the unseen test data. The precision, recall, and F1-scores were also well balanced between the two classes, indicating that the model performs consistently across both target categories.

The use of feature scaling and cross-validation helped create a more reliable modeling pipeline and reduced the risk of selecting a model configuration based only on a single train-test split.

Overall, this project demonstrates that Logistic Regression can provide strong and interpretable binary classification performance when the selected features contain meaningful information about the target variable.

However, the model's performance is specific to this dataset and the preprocessing decisions applied during the project. Testing the final model on completely independent data and considering additional relevant features could provide a more reliable assessment of its generalization capability.

Key Steps:

Data loading and inspection

Data cleaning and duplicate removal

Exploratory Data Analysis (EDA)

Identification and removal of invalid/suspicious observations

Feature selection

Feature standardization using StandardScaler

Train-test splitting

Logistic Regression with L2 regularization

Hyperparameter optimization using GridSearchCV

5-fold cross-validation

Model evaluation using Accuracy, Precision, Recall, and F1-Score

Final performance analysis
