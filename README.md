## Table of Contents
1. Introduction
2. MATERIALS AND METHODS
   
   A. Data Collection
   B. Data Preprocessing
   C. Model Selection
   D. Model Training and Testing
   E. Machine Learning Models
   F. Evaluation of F1 Scores
   G. Hyperparameter Tuning
   H. Identification of Impactful Personal Attributes
   I. Evaluation of Model Performance
   J. Assessment of Discrimination Ability
   K. Model Evaluation
   
4. RESULTS AND DISCUSSION
5. Conclusion
   - Implications
   - Recommendations

## Introduction

The introduction section provides an overview of the study, including the background, research objectives, and significance of the research topic.

## MATERIALS AND METHODS

### A. Data Collection

The data collection procedure for this study involved utilizing the annual BRFSS data in 2021 obtained from the Center for Disease Control (CDC). The dataset consisted of 438,693 records with 304 attributes, from which a specific subset of 19 attributes was chosen for analysis and model development.

### B. Data Preprocessing

The data preprocessing step involved tasks such as data cleaning, normalization, feature selection, and feature engineering to ensure the data's quality and suitability for machine learning algorithms.

### C. Model Selection

The appropriate machine learning algorithm(s) were selected based on the data characteristics and research question being addressed.

### D. Model Training and Testing

The data was divided into training and testing sets using an 80:20 ratio. The selected machine learning algorithm(s) were trained on the training set and evaluated on the testing set to assess their performance.

### E. Machine Learning Models

Several machine learning models, including Logistic Regression, K-Nearest Neighbor, Naive Bayes, Decision Tree Classifier, and Random Forest, were employed based on their appropriateness for classification tasks and ability to handle different types of variables.

### F. Evaluation of F1 Scores

The models' performance was evaluated using F1 scores, a metric combining precision and recall, through 10-fold cross-validation. The mean F1 score for each model was calculated to represent its overall performance.

### G. Hyperparameter Tuning

Hyperparameter tuning was performed to improve the model's performance. The regularization parameter C was tuned using GridSearchCV to identify the optimal setting.

### H. Identification of Impactful Personal Attributes

The coefficients of the model with the best F1 score were analyzed to determine the personal attributes that significantly influenced the risk prediction of cardiovascular diseases (CVDs).

### I. Evaluation of Model Performance

The performance of the model with the best F1 score was assessed using a confusion matrix to calculate metrics such as sensitivity and specificity.

### J. Assessment of Discrimination Ability

The model's ability to distinguish between healthy individuals and those at risk for CVDs was evaluated using the area under the curve (AUC) of the receiver operating characteristics (ROC) curve.

### K. Model Evaluation

The final step involved evaluating the performance of the machine learning algorithm(s) using various statistical tools, including accuracy, precision, recall, F1-score, ROC curve, and AUC.

## RESULTS AND DISCUSSION

This section presents the results of the study and provides a comprehensive discussion and analysis of the findings.

## Conclusion

The conclusion section summarizes the key findings of the study and presents implications and recommendations based on the research outcomes.

- Implications: This subsection discusses the implications of the study's findings and their potential impact on the field or relevant stakeholders.

