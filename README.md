### Table of Contents
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

### Introduction

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

### RESULTS AND DISCUSSION

In this study, a series of tests were conducted to compare the effectiveness of different machine learning (ML) models in predicting cardiovascular diseases (CVDs). The ML algorithms were implemented on an Intel Core i7 8th generation machine with the Windows 10 operating system, using R Studio and Python with learn packages such as Pandas, NumPy, and Sci-kit learn. The models were trained on a training set and evaluated on a separate test set to assess their performance.

To ensure a balanced evaluation of the models, the F1 score was chosen as the metric, which considers both precision and recall. Cross-validation was employed using a 10-Stratified K-Fold, and the mean F1 score was calculated to represent the overall performance of each model. The ML models used in this study included Logistic Regression (LR), Gaussian Naive Bayes (NB), Decision Tree Classifier (DT), K-Nearest Neighbor (KNN), and Random Forest (RF).

Table I presents the performance of the ML models using the 10-fold cross-validation and F1 scores as the metric. The mean F1 score for each model is calculated to represent its overall performance. The results in Table I indicate that the Logistic Regression model achieved the highest mean F1 score of 0.32564, followed by K-Nearest Neighbor with a score of 0.27350. Naïve Bayes, Decision Tree Classifier, and Random Forest models achieved lower F1 scores.

To further analyze the performance of the models, a classification report was generated for the training set, as shown in the tables. The Logistic Regression model achieved the highest F1 score of 0.3257 in the training data. However, it is worth noting that the Decision Tree Classifier achieved a high F1 score of 0.99. Despite this, the Decision Tree model was not considered suitable for this study because the mean F1 score in the cross-validated results differed significantly from the F1 score in the training set, suggesting overfitting.

The researcher then focused on tuning the hyperparameters of the Logistic Regression model to improve its performance. The hyperparameter tuned was the regularization parameter C, which controls the tradeoff between fitting the training data and model complexity. The GridSearchCV technique was used with three values of C: 0.1, 1, and 10. The mean F1 scores for each C value on the training and test sets are presented in Table VII. The best-performing model was found with C = 0.1, achieving a mean F1 score of 0.3257. Using the Logistic Regression model with the optimal hyperparameter setting (C = 0.1), the classification report for the test set was generated and shown in Table VIII.

The model achieved an F1 score of 0.33, which is consistent with the F1 score obtained in the training data, indicating good generalization ability.

The feature importance analysis provides valuable insights into the variables that significantly contribute to the model's predictions. Among the variables, the categorical variable "Sex" exhibited the highest feature importance. The Logistic Regression model assigns more weight to males compared to females when predicting the risk of CVDs. The variable "Diabetes" also had positive importance, indicating that individuals identified as diabetic are considered at higher risk. Conversely, the variable "General Health" had the highest negative importance, suggesting that individuals reporting poor general health are considered more at risk for CVDs.

Furthermore, the performance of the Logistic Regression model on the unknown data was further examined using a confusion matrix. The model correctly classified 79.18% of individuals with CVDs and 73.46% of healthy individuals, indicating a high level of accuracy in identifying individuals at risk for CVDs and distinguishing them from those who are healthy.

The area under the curve (AUC) of the receiver operating characteristics (ROC) curve was computed as a performance metric for the Logistic Regression model. The AUC value, which measures the degree of separability between classes, was found to be 0.837, indicating that the model is effective in predicting healthy individuals as healthy and individuals at risk for CVDs as being at risk.

Overall, the results demonstrate that the Logistic Regression model, with a tuned hyperparameter C = 0.1, exhibits a good level of performance on the unknown test data. It successfully predicts the risk of CVDs, as indicated by high values of sensitivity, specificity, and AUC. The feature importance analysis provides valuable insights into the variables that significantly contribute to the model's predictions, highlighting the importance of sex, diabetes, and general health in assessing the risk of CVDs. These findings contribute to a better understanding of the factors associated with CVD risk and can assist in developing targeted interventions and preventive measures.

### Conclusion

The study concludes that the Logistic Regression (LR) model outperforms other machine learning models in predicting CVD risk based on personal lifestyle factors. It achieves the highest mean F1 score among the evaluated models. The LR model is fine-tuned using hyperparameter tuning techniques, resulting in improved predictive performance. The evaluation on the test data demonstrates the model's consistency and reliability.

Feature importance analysis reveals that sex, diabetes, and general health have significant impacts on CVD risk prediction according to the LR model. The model shows high accuracy in classifying individuals with CVDs and healthy individuals, and its AUC score confirms its effectiveness in distinguishing between the two classes.

The findings of the study have practical implications for healthcare professionals, researchers, and policymakers. The LR model can be incorporated into clinical practice for early detection and personalized interventions. The identified influential personal attributes can guide the development of targeted intervention strategies. The study enriches the existing knowledge on CVD risk prediction and contributes to improved patient outcomes and reduced CVD-related morbidity and mortality.

- The study's implications are as follows:

The Logistic Regression model demonstrates superior performance in predicting CVD risk compared to other machine learning models. Healthcare professionals and researchers can utilize this model for effective CVD risk prediction based on personal lifestyle factors. The comprehensive evaluation and comparison of different machine learning models provide insights into the most suitable models for CVD risk prediction. This information aids in selecting the appropriate model for specific tasks. The study highlights the importance of model evaluation and the impact of hyperparameter tuning. It emphasizes the need for caution when interpreting model results and the value of cross-validation techniques for assessing generalization ability. The identified influential personal attributes, such as sex, diabetes, and general health, offer valuable insights for healthcare professionals. These attributes can inform targeted interventions and personalized preventive measures for individuals at risk of developing CVDs. The Logistic Regression model demonstrates high accuracy in classifying individuals with CVDs and healthy individuals. Sensitivity, specificity, and AUC values further validate its predictive capabilities. This enables effective risk identification and personalized interventions. The study showcases the potential of machine learning and electronic health records in analyzing large datasets for identifying CVD risk factors. It emphasizes the importance of data-driven approaches in healthcare research and decision-making.

- Recommendations:

Based on the study findings, the following recommendations are made:

Incorporate machine learning models, specifically the Logistic Regression model, into clinical practice for CVD risk prediction based on personal lifestyle factors. This facilitates early detection, prevention, and personalized treatment strategies. Validate the Logistic Regression model on diverse datasets to ensure its generalizability and robustness. Evaluating its performance on different populations and healthcare settings enhances its applicability. Explore additional personal attributes and data sources to improve CVD risk prediction. Investigate variables like age, BMI, smoking status, and genetic markers. Integrate data from wearable devices and genetic databases for richer information.  Continuously refine and update the predictive model to incorporate advancements in machine learning. Regularly reassess the model's performance, incorporate new features or algorithms, and enhance its accuracy and predictive power. Conduct prospective studies to assess the real-world impact of the Logistic Regression model in clinical practice. Evaluate its effectiveness, address challenges or limitations, and ensure seamless integration into healthcare workflows. Collaborate with stakeholders, including researchers, healthcare providers, policymakers, and technology experts, to implement the predictive model effectively. Develop guidelines, protocols, and decision support systems that leverage the model for improved patient outcomes and preventive measures.  Promote awareness and education on CVD risk factors, emphasizing attributes such as sex, diabetes, and general health. Launch educational campaigns, interventions, and lifestyle modification programs to empower individuals in mitigating their CVD risk.  Prioritize data privacy and ethical considerations when working with personal health data. Safeguard patient confidentiality, obtain informed consent, and implement robust data governance practices to ensure ethical use of data in CVD risk prediction. By implementing these recommendations, healthcare systems, and practitioners can leverage machine learning to enhance CVD risk prediction, improve patient care, and reduce the burden of cardiovascular diseases.
