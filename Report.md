# Module 20 Report - Credit Risk Analysis

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).

The aim of this study is to assess how effectively two machine learning models based on logistic regression can predict the credit risk connected with loans. The study involved examining financial data related to factors such as loan amounts, interest rates, borrowers' income, debt-to-income ratios, account numbers, derogatory marks, and overall debt. The primary goal was to anticipate the status of loans, which could either be classified as sound loans ('0') or high-risk loans ('1').

* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

The steps of this machine learning procedure comprised the subsequent stages:
1. Dividing the datasets into segments for training and testing purposes.
2. Formulating and applying a logistic regression model using the available data.
3. Appraising the model's effectiveness by examining metrics such as accuracy, precision, recall, and f1 scores.
4. Adjusting the dataset distribution using Random Over Sampler to address class imbalance.
5. Constructing and fitting an additional logistic regression model using the rebalanced data.
6. Assessing the secondary model's performance using the identical set of metrics: accuracy, precision, recall, and f1 scores.


## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.

* Accuracy: The accuracy of the model is 0.99, meaning that it correctly classifies 99% of the instances.
* Precision:
  For healthy loans ('0'): The model has a precision of 1.00, meaning that it perfectly identifies true positives with no false positives.
  For high-risk loans ('1'): The model has a precision of 0.87, meaning that it is moderately effective in identifying high-risk loans with some false positives.
* Recall:
  For healthy loans ('0'): The model has a recall of 1.00, meaning that it perfectly identifies all instances of healthy loans with no false negatives.
  For high-risk loans ('1'): The model has a recall of 0.89, meaning that it is moderately effective in identifying high-risk loans with some false negatives.

* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.

* Accuracy: The accuracy of the model is 0.99, meaning that it correctly classifies 99% of the instances.
* Precision:
  For healthy loans ('0'): The model has a precision of 0.99, meaning that it is almost perfect at identifying true positives with few false positives.
  For high-risk loans ('1'): The model has a precision of 0.99, meaning that it is almost perfect at identifying high-risk loans with few false positives. 
* Recall:
  For healthy loans ('0'): The model has a recall of 0.99, meaning that it is almost perfect at identifying nearly all instances of healthy loans with few false negatives.
  For high-risk loans ('1'): The model has a recall of 0.99, meaning that it is almost perfect at identifying high-risk loans with few false negatives.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.

Upon reviewing the outcomes of the modeling process, I concluded that the secondary logistic regression model, trained with resampled data, outperformed the initial model trained with the original dataset. This was especially evident in its ability to predict high-risk loans ('1'). The secondary model exhibited enhanced precision, recall, and f1 scores for high-risk loans, a critical aspect for aiding the lending company in mitigating the occurrence of non-performing loans and subsequent financial setbacks.

Based on these observations, I strongly recommend the adoption of the second model, employing logistic regression and trained on resampled data, for this credit risk analysis. The improved accuracy and results, compared to the initial model, indicate its efficacy. The outcomes demonstrate its capacity to more accurately distinguish between healthy loan applications and high-risk loan applications, thus helping prevent the issuance of loans that could lead to substantial future losses.
