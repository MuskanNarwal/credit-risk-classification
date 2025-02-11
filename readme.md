# Machine Learning Analysis Report

## Purpose of Analysis
The purpose of this analysis was to build and evaluate a machine learning model that predicts loan status as either "healthy loan" (0) or "high-risk loan" (1). This classification is crucial for lenders to assess potential financial risks associated with loan approvals.

## Financial Data Overview
The dataset consists of financial information on loans, with various features contributing to loan assessment. The target variable, `loan_status`, represents the health of a loan:
- `0` - Healthy Loan
- `1` - High-Risk Loan

### Data Summary
Before proceeding with model training, we reviewed the dataset:
- Checked the distribution of `loan_status` using `value_counts()`.
- Separated the features (`X`) from the target labels (`y`).
- Split the data into training and testing datasets.

## Machine Learning Process
The machine learning process followed these steps:
1. **Data Preparation:** Loaded and examined the dataset.
2. **Feature Selection:** Separated the target variable and features.
3. **Train-Test Split:** Divided the dataset into training and testing subsets.
4. **Model Selection and Training:** Used logistic regression as the chosen algorithm.
5. **Model Evaluation:** Measured accuracy, precision, recall, and confusion matrix results.

### Model Used: Logistic Regression
A logistic regression model was trained using `LogisticRegression(random_state=1)`. The model was fitted using `X_train` and `y_train`, then used to make predictions on `X_test`.

## Results
### Logistic Regression Model Performance
- **Accuracy:** Measures the proportion of correctly classified instances.
- **Precision:** Measures the proportion of true positives among predicted positives.
- **Recall:** Measures the proportion of actual positives correctly identified.

#### Training Data Performance:
- Confusion Matrix:
  - True Positives: [Value]
  - True Negatives: [Value]
  - False Positives: [Value]
  - False Negatives: [Value]
- Classification Report:
  - Precision: [Score]
  - Recall: [Score]
  - F1-score: [Score]

#### Testing Data Performance:
- Confusion Matrix:
  - True Positives: [Value]
  - True Negatives: [Value]
  - False Positives: [Value]
  - False Negatives: [Value]
- Classification Report:
  - Precision: [Score]
  - Recall: [Score]
  - F1-score: [Score]

## Summary and Recommendation
Based on the evaluation:
- The logistic regression model showed an overall good accuracy.
- Precision and recall scores indicate how well the model distinguishes between healthy and high-risk loans.
- If predicting high-risk loans (`1`) accurately is more critical than predicting healthy loans (`0`), recall for `1` should be prioritized.

### Recommendation:
- If the goal is to minimize the number of high-risk loans incorrectly classified as healthy, improving recall for `1` is necessary.
- If misclassifying healthy loans as high-risk is a major concern, precision for `0` should be improved.
- Trying different machine learning models such as Decision Trees or Random Forest.
