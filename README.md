
# Breast Cancer Prediction Using Logistic Regression

This project aims to build a predictive model to classify breast cancer as malignant or benign using the `Logistic Regression` algorithm. The dataset used for this analysis is the Breast Cancer Wisconsin dataset, which is part of the `sklearn` library.

## Steps in the Model

### 1. Data Loading and Exploration

- **Dataset:** The Breast Cancer Wisconsin dataset from `sklearn.datasets` is loaded.
- **DataFrame Creation:** The features and target are converted into two separate pandas DataFrames: `df_features` for the input variables and `df_target` for the output variable (target).
- **Missing Values Check:** A check is performed to ensure there are no missing values in the dataset.

### 2. Data Visualization

- **Histograms:** 
  - The distribution of two selected features (`mean radius` and `mean texture`) is visualized using histograms to understand their spread and central tendencies.
- **Correlation Matrix:**
  - A heatmap of the correlation matrix of all features is plotted to observe the relationships between different features.
  - Highly correlated features (correlation > 0.9) are identified and visualized using another heatmap.

### 3. Balance of Target Variable

- A count plot is used to visualize the balance of the target variable, which helps in understanding the distribution of malignant and benign cases.

### 4. Data Preparation

- **Data Splitting:**
  - The dataset is split into training and testing sets with an 80-20 ratio using `train_test_split` while maintaining the class proportions with `stratify`.
- **Feature Normalization:**
  - The feature values are normalized using `StandardScaler` to ensure all features contribute equally to the model training.

### 5. Model Training and Evaluation

- **Logistic Regression Model:**
  - A logistic regression model is trained on the normalized training data.
- **Model Evaluation:**
  - The model's accuracy is evaluated using the test data.
  - A confusion matrix and classification report are generated to assess the performance of the model, including precision, recall, and F1-score.
- **Feature Importance:**
  - The coefficients of the logistic regression model are used to identify the top 3 most important features contributing to the prediction of malignancy.

### 6. Feature Selection and Hyperparameter Tuning

- **Feature Selection:**
  - Recursive Feature Elimination (RFE) is used to select the top 10 features that are most significant for the model.
- **Hyperparameter Tuning:**
  - `GridSearchCV` is used to find the best hyperparameters (`C` values for regularization) for the logistic regression model.
- **Improved Model Evaluation:**
  - The tuned model is evaluated again using the test data to compare the performance against the initial model.

## Results

- **Initial Model Accuracy:** Displays the accuracy, confusion matrix, and classification report for the initial logistic regression model.
- **Improved Model Accuracy:** Shows the performance metrics for the improved model after feature selection and hyperparameter tuning.

## Conclusion

This project demonstrates a complete workflow for building and optimizing a logistic regression model for breast cancer prediction. The results indicate the importance of feature selection and hyperparameter tuning in improving the model's performance.
