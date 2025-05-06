# Assignment 5: Health Data Classification Results

This file contains your manual interpretations and analysis of the model results from the different parts of the assignment.

## Part 1: Logistic Regression on Imbalanced Data

### Interpretation of Results

In this section, provide your interpretation of the Logistic Regression model's performance on the imbalanced dataset. Consider:

- Which metric performed best and why?
- Which metric performed worst and why?
- How much did the class imbalance affect the results?
- What does the confusion matrix tell you about the model's predictions?

**Evaluation Metrics:**

- **Accuracy:** 0.9168  
- **Precision:** 0.6615  
- **Recall:** 0.3007  
- **F1 Score:** 0.4135  
- **AUC:** 0.6420  
- **Confusion Matrix:**: [[1301, 22], [100, 43]]

**Interpretation:**

The Logistic Regression model achieved high accuracy (91.68%) and precision (66.15%), indicating it correctly identified a large number of negative cases. However, the recall was  low at 30.07%, suggesting that the model failed to identify a significant portion of positive cases. This disparity is likeley due to class imbalance, as shown by the confusion matrix, where the model is biased towards the majority class. 

**Imbalance Impact Score:** 0.70  
*This score reflects the degree to which class imbalance affected model performance, with 1 indicating maximum impact. At a score of 0.70, class imbalance significantly affected model perfomance.*

## Part 2: Tree-Based Models with Time Series Features

### Comparison of Random Forest and XGBoost

In this section, compare the performance of the Random Forest and XGBoost models:

- Which model performed better according to AUC score?
- Why might one model outperform the other on this dataset?
- How did the addition of time-series features (rolling mean and standard deviation) affect model performance?


**AUC Scores:**

- **Random Forest:** 0.9984  
- **XGBoost:** 1.0000

**Interpretation:**

Incorporating time series features such as rolling mean and standard deviation of heart rate significantly enhanced model performance. Both Random Forest and XGBoost models achieved near-perfect AUC scores. XGBoost, in particular, achieved a perfect AUC of 1.0000.

## Part 3: Logistic Regression with Balanced Data

### Improvement Analysis

In this section, analyze the improvements gained by addressing class imbalance:

- Which metrics showed the most significant improvement?
- Which metrics showed the least improvement?
- Why might some metrics improve more than others?
- What does this tell you about the importance of addressing class imbalance?

*Your analysis here...*

## Overall Conclusions

Summarize your key findings from all three parts of the assignment:

- What were the most important factors affecting model performance?
- Which techniques provided the most significant improvements?
- What would you recommend for future modeling of this dataset?

**Evaluation Metrics:**

- **Accuracy:** 0.8450  
- **Precision:** 0.3935  
- **Recall:** 0.8777  
- **F1 Score:** 0.5434  
- **AUC:** 0.9133  
- **Confusion Matrix:** [[996, 188],[17, 122]]

**Interpretation:**

Applying SMOTE to balance the dataset before training the Logistic Regression model led to a significant improvement in recall (from 30.07% to 87.77%). While precision decreased to 39.35%, the overall F1 Score and AUC improved, suggesting a better balance between precision and recall and improved overall model performance.


**Percentage Improvements:**

- **Recall:** +191.8%  
- **F1 Score:** +31.4%  
- **AUC:** +42.3%  
- **Precision:** -40.5%  
- **Accuracy:** -7.8%

**Interpretation:**

Balancing the dataset using SMOTE led to a dramatic increase in recall, which is helpful for applications where identifying positive cases is particularly important. Although precision and accuracy decreased, the trade-off resulted in a more balanced model, as shown by the improved F1 Score and AUC.



