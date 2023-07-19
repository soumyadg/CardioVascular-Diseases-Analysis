# CardioVascular-Diseases-Analysis

Table of Contents
Introduction
MATERIALS AND METHODS
A. Data Collection
The data collection procedure for this study involved utilizing the annual BRFSS data in 2021 obtained from the Center for Disease Control (CDC). The dataset, which consisted of 438,693 records with a total of 304 attributes, was accessed on a local machine. However, not all attributes were relevant to this particular study. Consequently, a specific subset of 19 attributes was chosen and incorporated into the construction of the machine learning (ML) model to create the predictive model for cardiovascular disease (CVD). This deliberate selection led to a reduction in the number of records, resulting in a total of 308,854 data instances utilized for analysis and model development.

B. Data Preprocessing
The next step involved preprocessing the data to ensure its readiness for the application of machine learning algorithms. This process entailed performing tasks such as data cleaning, normalization, feature selection, and feature engineering. These measures were taken to optimize the quality and suitability of the data for subsequent analysis and model development.

C. Model Selection
The next step involved selecting the appropriate machine learning algorithm(s) for the data, considering the specific variables being used and the research question being addressed. This decision was made based on careful consideration of the data characteristics and the desired outcomes of the study.

D. Model Training and Testing
After selecting the machine learning algorithm(s), the data was divided into training and testing sets using an 80:20 ratio. The training set consisted of 80% of the data, while the remaining 20% was allocated for testing. The selected machine learning algorithm(s) were trained using the training set and subsequently evaluated using the testing set to evaluate their performance.

E. Machine Learning Models
Several machine learning models were employed, such as Logistic Regression, K-Nearest Neighbor, Naive Bayes, Decision Tree Classifier, and Random Forest. These models were selected based on their appropriateness for classification tasks and their capability to handle both numerical and categorical variables.

F. Evaluation of F1 Scores
To identify the model achieving the best F1 score in predicting CVD risk, a comprehensive evaluation was performed using 10-fold cross-validation. F1 scores, a metric combining precision and recall, were used to assess the models’ performance. The mean F1 score for each model was calculated to represent its overall performance.

G. Hyperparameter Tuning
In the process of identifying impactful personal attributes for predicting CVD risk, the coefficients associated with the best F1 score were analyzed. The magnitude and direction of these coefficients were examined to determine the influence of different personal attributes on the model’s predictions. Specifically, the variables ”Sex,” ”Diabetes,” and ”General Health” were considered. The model was improved through hyperparameter tuning, focusing on the regularization parameter C. GridSearchCV, a technique that systematically tested different values of the hyperparameter, was employed. The values of C evaluated were 0.1, 1, and 10, aiming to identify the optimal setting that enhanced the model’s performance.

H. Identification of Impactful Personal Attributes
The coefficients of the model with the best F1 score were examined to determine the personal attributes that significantly influenced the risk prediction of CVDs. Feature importance was derived from the magnitude and direction of the coefficients. Variables with higher coefficients were considered to have a greater impact on the model’s predictions.

I. Evaluation of Model Performance
The performance of the model with the best F1 score was assessed by examining its ability to correctly classify individuals with CVDs and healthy individuals. A confusion matrix was employed to calculate true positive, true negative, false positive, and false negative values. Sensitivity (recall) and specificity were derived from these values to determine the model’s accuracy.

J. Assessment of Discrimination Ability
The model’s ability to distinguish between classes was evaluated using the area under the curve (AUC) of the receiver operating characteristics (ROC) curve. The AUC score quantifies the model’s separability in distinguishing healthy individuals from those at risk for CVDs. The methodology employed in this study provided a comprehensive approach to predict CVD risk using machine learning models. By evaluating performance metrics, conducting hyperparameter tuning, analyzing feature importance, and assessing model accuracy and discrimination ability, the study aimed to enhance understanding of the role of personal attributes in predicting CVD risk.

K. Model Evaluation
The final step involved evaluating the performance of the machine learning algorithm(s) using various statistical tools, including accuracy, precision, recall, F1-score, receiver operating characteristic (ROC) curve, and area under the curve (AUC). These metrics were calculated to assess the performance of the machine learning algorithm(s) on the test data.

RESULTS AND DISCUSSION
In this study, a series of tests were conducted to compare the effectiveness of different machine learning (ML) models in predicting cardiovascular diseases (CVDs). The ML algorithms were implemented on an Intel Core i7 8th generation machine with the Windows 10 operating system, using R Studio and Python with learn packages such as Pandas, NumPy, and Sci-kit learn. The models were trained on a training set and evaluated on a separate test set to assess their performance.

To ensure a balanced evaluation of the models, the F1 score was chosen as the metric, which considers both precision and recall. Cross-validation was employed using a 10-Stratified K-Fold, and the mean F1 score was calculated to represent the overall performance of each model. The ML models used in this study included Logistic Regression (LR), Gaussian Naive Bayes (NB), Decision Tree Classifier (DT), K-Nearest Neighbor (KNN), and Random Forest (RF).

TABLE I: PERFORMANCE OF MACHINE LEARNING (ML) MODELS USING THE 10-FOLD CROSS-VALIDATION
Model     F1
1 Logistic Regression    0.32564
2 Naive Bayes    0.26982
3 Decision Tree Classifier    0.22237
4 K Neighbors Classifier    0.27350
5 Random Forest Classifier    0.17830

Table I presents the performance of the ML models using the 10-fold cross-validation and F1 scores as the metric. The mean F1 score for each model is calculated to represent its overall performance. The results in Table I indicate that the Logistic Regression model achieved the highest mean F1 score of 0.32564, followed by K-Nearest Neighbor with a score of 0.27350. Naïve Bayes, Decision Tree Classifier, and Random Forest models achieved lower F1 scores.

TABLE II: CLASSIFICATION REPORT OF LOGISTIC REGRESSION MODEL ON TRAIN SET
precision    recall    f1-score    support
0    0.975126    0.731742    0.836082    227106.000000
1    0.205293    0.787806    0.325710    19977.000000
accuracy    0.736275    0.736275    0.736275    0.736275
macro avg    0.590210    0.759774    0.580896    247083.000000
weighted avg    0.912884    0.736275    0.794818    247083.000000

To further analyze the performance of the models, a classification report was generated for the training set, as shown in Table II. The Logistic Regression model achieved the highest F1 score of 0.3257 in the training data. However, it is worth noting that the Decision Tree Classifier achieved a high F1 score of 0.99. Despite this, the Decision Tree model was not considered suitable for this study because the mean F1 score in the cross-validated results differed significantly from the F1 score in the training set, suggesting overfitting.

TABLE III: CLASSIFICATION REPORT OF DECISION TREE MODEL ON TRAIN SET
precision    recall    f1-score    support
0    0.999982    1.000000    0.999991    227106.000000
1    1.000000    0.999800    0.999900    19977.000000
accuracy    0.999984    0.999984    0.999984    0.999984
macro avg    0.999991    0.999900    0.999946    247083.000000
weighted avg    0.999984    0.999984    0.999984    247083.000000

TABLE IV: CLASSIFICATION REPORT OF RANDOM FOREST MODEL ON TRAIN SET
precision    recall    f1-score    support
0    0.999974    0.999996    0.999985    227106.000000
1    0.999950    0.999700    0.999825    19977.000000
accuracy    0.999972    0.999972    0.999972    0.999972
macro avg    0.999962    0.999848    0.999905    247083.000000
weighted avg    0.999972    0.999972    0.999972    247083.000000

TABLE V: CLASSIFICATION REPORT OF K-NEAREST NEIGHBOR MODEL ON TRAIN SET
precision    recall    f1-score    support
0    0.999984    0.840867    0.913549    227106.000000
1    0.355954    0.999850    0.525003    19977.000000
accuracy    0.853721    0.853721    0.853721    0.853721
macro avg    0.677969    0.920359    0.719276    247083.000000
weighted avg    0.947914    0.853721    0.882135    247083.000000

TABLE VI: CLASSIFICATION REPORT OF NAÏVE BAYES MODEL ON TRAIN SET
precision    recall    f1-score    support
0    0.975800    0.625329    0.762207    227106.000000
1    0.162046    0.823697    0.270815    19977.000000
accuracy    0.641367    0.641367    0.641367    0.641367
macro avg    0.568923    0.724513    0.516511    247083.000000
weighted avg    0.910007    0.641367    0.722478    247083.000000

TABLE VII: HYPERPARAMETER TUNING OF LOGISTIC REGRESSION
C    Mean Score of Train Set    Mean Score of Test Set
0.1    0.3259    0.3257
1    0.3259    0.26982
10    0.3259    0.3256

The researcher then focused on tuning the hyperparameters of the Logistic Regression model to improve its performance. The hyperparameter tuned was the regularization parameter C, which controls the tradeoff between fitting the training data and model complexity. The GridSearchCV technique was used with three values of C: 0.1, 1, and 10. The mean F1 scores for each C value on the training and test sets are presented in Table VII. The best-performing model was found with C = 0.1, achieving a mean F1 score of 0.3257 . Using the Logistic Regression model with the optimal hyperparameter setting (C = 0.1), the classification report for the test set was generated and shown in Table VIII.

TABLE VIII: CLASSIFICATION REPORT OF LOGISTIC REGRESSION MODEL ON TEST SET
precision    recall    f1-score    support
0    0.98    0.73    0.84    56777
1    0.21    0.79    0.33    4994
accuracy    0.74    0.74    0.74    61771
macro avg    0.59    0.76    0.58    61771
weighted avg    0.91    0.74    0.80    61771

The model achieved an F1 score of 0.33, which is consistent with the F1 score obtained in the training data, indicating good generalization ability.

Sex
Diabetes Yes
Smoking History
Arthritis
Age Category
Depression
Exercise
Weight
Green Vegetables Consumption
BMI
Fruit Consumption
Fried Potato Consumption
Skin Cancer
Other Cancer Type
Height
Alcohol Consumption
Diabetes Yes During Pregnancy
Diabetes No, Pre-Diabetes
Check-up Status
General Health
-0.6    -0.4    -0.2    0.0    0.2    0.4    0.6    0.8    1.0

Fig. 1. Feature Importance

To understand the importance of features in the Logistic Regression model, feature importance based on the coefficients of the model’s equation was examined. Standardization was applied to put all variables in the same scale, and the feature importance results are presented in Figure 1. The variable "Sex" had the highest positive feature importance, suggesting that the model considers men to be more at risk for cardiovascular diseases (CVDs) than women. The variable "Diabetes" also had positive importance, indicating that individuals identified as diabetic are considered at higher risk. Conversely, the variable "General Health" had the highest negative importance, suggesting that individuals reporting poor general health are considered more at risk for CVDs.

40000
35000
0
41712    15065
30000
Values
25000
Actual
20000
15000
1
1040    3954
10000
5000
0    1
Predicted Values

Fig. 2. Confusion Matrix

The performance of the Logistic Regression model on the unknown data was further examined using a confusion matrix, as shown in Figure 2. The true positive, true negative, false positive (Type 1 error), and false negative (Type 2 error) values were used to evaluate the model's performance. Sensitivity (recall) and specificity were calculated from these values, providing insight into the model's ability to correctly classify individuals with CVDs and healthy individuals. The sensitivity of the model was 0.79, indicating that it correctly identified 79% of individuals with CVDs. The specificity was 0.98, indicating that it correctly identified 98% of healthy individuals. The accuracy of the model was 0.74, indicating that it correctly predicted the CVD risk for 74% of the individuals in the test set.

CONCLUSION
The results of this study demonstrate that machine learning models can effectively predict cardiovascular disease (CVD) risk using personal attributes as inputs. Among the machine learning models tested, the Logistic Regression model performed the best, achieving an F1 score of 0.33 on the test set. The analysis of feature importance revealed that attributes such as "Sex," "Diabetes," and "General Health" significantly influenced the model's predictions. Men were considered to be at higher risk for CVDs, as were individuals with diabetes and those reporting poor general health.

The findings of this study have several implications. First, they suggest that machine learning models can serve as valuable tools in identifying individuals at risk for CVDs. This can aid healthcare professionals in developing targeted prevention and intervention strategies. Second, the identification of influential personal attributes provides insights into the factors contributing to CVD risk. This information can inform public health policies and initiatives aimed at reducing CVD prevalence. Third, the performance evaluation and analysis provide valuable insights into the strengths and limitations of different machine learning models for predicting CVD risk.

While this study provides promising results, several limitations should be acknowledged. The data used in this study was obtained from a specific source and may not be representative of the entire population. The selected attributes were limited in number and may not capture the full complexity of CVD risk factors. Future studies should consider incorporating a broader range of variables and utilizing data from diverse populations to enhance the generalizability of the findings.

In conclusion, this study demonstrates the potential of machine learning models in predicting CVD risk based on personal attributes. The findings contribute to the growing body of research in the field of predictive analytics and can guide the development of targeted interventions to reduce the burden of CVDs. Further research is warranted to refine the models, incorporate additional variables, and validate the findings in diverse populations.
