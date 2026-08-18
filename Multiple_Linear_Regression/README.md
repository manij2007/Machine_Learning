Mani-Jafari

This project implemented a Multiple Linear Regression model to predict students' Performance Index based on several academic and lifestyle-related features, including Hours Studied, Previous Scores, Extracurricular Activities, Sleep Hours, and Sample Question Papers Practiced.

The dataset initially contained 10,000 records. During preprocessing, 127 duplicate records were identified and removed, leaving 9,873 observations. No missing values were found. The categorical feature, Extracurricular Activities, was converted into numerical form using Label Encoding.

The dataset was divided into training and testing sets using an 80/20 split. A Multiple Linear Regression model with an intercept was then trained on the training data and evaluated on the unseen test set.

Model Performance:

MAE: 1.644

MSE: 4.266

RMSE: 2.065

R² Score: 0.9882

The model achieved an R² score of approximately 98.82%, indicating that the selected features explain a very large proportion of the variation in the Performance Index within this dataset. The relatively low MAE and RMSE also indicate that the model's predictions are generally close to the actual performance values.

The Actual vs. Predicted plot further demonstrates that the predictions closely follow the ideal prediction line, while the residual distribution provides an additional view of the model's prediction errors.

Overall, this project demonstrates that Multiple Linear Regression can be highly effective for predicting student performance when the available features have strong linear relationships with the target variable. However, the model's performance is specific to this dataset, and further validation on new or external data would be necessary to assess its generalization capability.

Key Steps:

Data loading and exploration

Duplicate removal and data validation

Exploratory Data Analysis (EDA)

Categorical feature encoding

Feature-target separation

Train-test splitting

Multiple Linear Regression training

Model evaluation using MAE, MSE, RMSE, and R²

Actual vs Predicted analysis

Residual analysis
