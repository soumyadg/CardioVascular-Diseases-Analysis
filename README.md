## Table of Contents
1. Introduction
2. MATERIALS AND METHODS
   
   - Data Collection
   - Data Preprocessing
   - Model Selection
   - Model Training and Testing
   - Machine Learning Models
   - Evaluation of F1 Scores
   - Hyperparameter Tuning
   - Identification of Impactful Personal Attributes
   - Evaluation of Model Performance
   - Assessment of Discrimination Ability
   - Model Evaluation
   
4. RESULTS AND DISCUSSION
5. Conclusion
   - Implications
   - Recommendations

## Introduction

The introduction section provides an overview of the study, including the background, research objectives, and significance of the research topic.

### MATERIALS AND METHODS

## A. Data Collection
The data collection procedure for this study involved utilizing the annual BRFSS data in 2021 obtained from the Center for Disease Control (2021). The dataset, which consisted of 438,693 records with a total of 304 attributes, was accessed on a local machine. However, not all attributes were relevant to this particular study. Consequently, a specific subset of 19 attributes was chosen and incorporated into the construction of the machine learning (ML) model to create the predictive model for cardiovascular disease (CVD). This deliberate selection led to a reduction in the number of records, resulting in a total of 308,854 data instances utilized for analysis and model development.

## B. Data Preprocessing
The next step involved preprocessing the data to ensure its readiness for the application of machine learning algorithms. This process entailed performing tasks such as data cleaning, normalization, feature selection, and feature engineering. These measures were taken to optimize the quality and suitability of the data for subsequent analysis and model development.

## C. Model Selection
The next step involved selecting the appropriate machine learning algorithm(s) for the data, considering the specific variables being used and the research question being addressed. This decision was made based on careful consideration of the data characteristics and the desired outcomes of the study.

## D. Model Training and Testing
After selecting the machine learning algorithm(s), the data was divided into training and testing sets using an 80:20 ratio. The training set consisted of 80% of the data, while the remaining 20% was allocated for testing. The selected machine learning algorithm(s) were trained using the training set and subsequently evaluated using the testing set to evaluate their performance.

## E. Machine Learning Models
Several machine learning models were employed, such as Logistic Regression, K-Nearest Neighbor, Naive Bayes, Decision Tree Classifier, and Random Forest. These models were selected based on their appropriateness for classification tasks and their capability to handle both numerical and categorical variables.

## F. Evaluation of F1 Scores
To identify the model achieving the best F1 score in predicting CVD risk, a comprehensive evaluation was performed using 10-fold cross-validation. F1 scores, a metric combining precision and recall, were used to assess the models' performance. The mean F1 score for each model was calculated to represent its overall performance.

## G. Hyperparameter Tuning
In the process of identifying impactful personal attributes for predicting CVD risk, the coefficients associated with the best F1 score were analyzed. The magnitude and direction of these coefficients were examined to determine the influence of different personal attributes on the model's predictions. Specifically, the variables "Sex," "Diabetes," and "General Health" were considered. The model was improved through hyperparameter tuning, focusing on the regularization parameter C. GridSearchCV, a technique that systematically tested different values of the hyperparameter, was employed. The values of C evaluated were 0.1, 1, and 10, aiming to identify the optimal setting that enhanced the model's performance.

## H. Identification of Impactful Personal Attributes
The coefficients of the model with the best F1 score were examined to determine the personal attributes that significantly influenced the risk prediction of CVDs. Feature importance was derived from the magnitude and direction of the coefficients. Variables with higher coefficients were considered to have a greater impact on the model's predictions.

## I. Evaluation of Model Performance
The performance of the model with the best F1 score was assessed by examining its ability to correctly classify individuals with CVDs and healthy individuals. A confusion matrix was employed to calculate true positive, true negative, false positive, and false negative values. Sensitivity (recall) and specificity were derived from these values to determine the model's accuracy.

## J. Assessment of Discrimination Ability
The model's ability to distinguish between classes was evaluated using the area under the curve (AUC) of the receiver operating characteristics (ROC) curve. The AUC score quantifies the model's separability in distinguishing healthy individuals from those at risk for CVDs. The methodology employed in this study provided a comprehensive approach to predict CVD risk using machine learning models. By evaluating performance metrics, conducting hyperparameter tuning, analyzing feature importance, and assessing model accuracy and discrimination ability, the study aimed to enhance understanding of the role of personal attributes in predicting CVD risk.

## K. Model evaluation
The final step involved evaluating the performance of the machine learning algorithm(s) using various statistical tools, including accuracy, precision, recall, F1-score, receiver operating characteristic (ROC) curve, and area under the curve (AUC). These metrics were calculated to assess the performance of the machine learning algorithm(s) on the test data.

## RESULTS AND DISCUSSION

This section presents the results of the study and provides a comprehensive discussion and analysis of the findings.

## Conclusion

The conclusion section summarizes the key findings of the study and presents implications and recommendations based on the research outcomes.

- Implications: This subsection discusses the implications of the study's findings and their potential impact on the field or relevant stakeholders.

