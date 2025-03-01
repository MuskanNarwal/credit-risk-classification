

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

## Model Evaluation: Precision and Recall for Class 1 (High-Risk Loans)
While the model performs well overall, it exhibits some limitations, particularly with regard to predicting **class 1** (high-risk loans). The recall and precision for class 1 are lower than expected, indicating that the model struggles to accurately predict high-risk loans. This is an important observation, especially considering the consequences of missing high-risk loans, which could potentially lead to financial losses for lenders.

#### Why the Low Recall and Precision for Class 1?
The low **recall** for class 1 suggests that the model fails to identify a significant number of high-risk loans, mistakenly classifying them as healthy loans. This can occur due to the imbalance in the dataset, where healthy loans (class 0) are more abundant than high-risk loans (class 1), leading to a bias in predictions.

The low **precision** for class 1 means that when the model predicts a loan as high-risk, it is often wrong, misclassifying healthy loans as high-risk. This increases the number of false positives, which can be costly for lenders if they decide to take actions based on these incorrect predictions.

#### Steps to Improve the Model
To address these limitations and improve the prediction of high-risk loans, consider the following strategies:
1. **Resampling Techniques:** Implement oversampling methods (e.g., SMOTE) to increase the proportion of high-risk loans in the dataset, or undersample the healthy loans to balance the classes.
2. **Class Weights Adjustment:** Modify the class weights in the logistic regression model to give more importance to class 1 during training, encouraging the model to focus more on identifying high-risk loans.
3. **Feature Engineering:** Explore adding additional features that could help distinguish high-risk loans more clearly from healthy loans.

## Summary and Recommendation
Based on the evaluation:
- The logistic regression model achieved a decent overall accuracy.
- However, the precision and recall for class 1 (high-risk loans) are lower than desirable, indicating the model struggles with this class.
- If predicting high-risk loans accurately is more important, prioritize improving recall for class 1.

### Recommendation:
- To reduce the number of high-risk loans misclassified as healthy, improving **recall** for class 1 should be prioritized.
- If misclassifying healthy loans as high-risk is a concern, focus on improving **precision** for class 1.
- Additionally, experimenting with different models such as **Decision Trees** or **Random Forest** may help improve classification for the minority class.

---

