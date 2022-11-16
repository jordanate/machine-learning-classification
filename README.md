# Phase 3 Machine Learning Classification Project - Stroke Dataset

## Overview

## Business Understanding

## Data Understanding

The data that we use for our project comes from a dataset from Kaggle titled, 'Stroke Prediction Dataset'. This source is comprised of basic life and health information from various individuals - some who have had a stroke and many who have not - such as age, BMI, presence of heart disease, type of work, and martial status.

## Modeling

After doing some data cleaning, We perform a 80%-20% Train-Test Split on the data with a history of stroke as the target variable and all other variables as the predictors. Next, We create several classification models.

Recall was the main metric used to determine the accuracy of our model due to the fact that we are interested in using our model to detect stroke risk, and therefore, a false negative is more costly than a false positive.

False Negatives are individiauls who were said to not have had a stroke but did.

False Positives are individuals who were said to have had a stroke but did not.

The following models were used on the testing set:

1. Logistic Regression (with and without optimal threshold)
2. Decision Tree
3. Tuned KNN (K-Nearest Neighbors)
4. Tuned Random Forest Classifier
5. Tuned XGBoost
6. Gaussian Naive Bayes

## Evaluation



### Why did we chose the Logistic Regression model (recall of 92%) rather than the Gaussian Naive Bayes model (recall of 94%) as our final model?
Although our main priority of this project was to minimize recall, the false positive rate that came with our highest recall outcome was too high for comfort. More specifically, the model that had the best recall was our Gaussian Naive Bayes model with a recall score of 0.94 but a false positive rate of 0.60. In comparison, our Logistic Regression model with the optimal threshold had a recall score of 0.92 with a false positive rate of 0.29.

Therefore, we decided that we are willing to risk a 0.02 difference in our recall for the sake of having a false positive rate that is more than half the size of that of the model with the best recall score.

Since our model would be a preliminary screening, part of the logic behind this decision is that we would like to lower the likelihood of causing someone who tests positive for stroke risk but is not actually at such risk (false positive) to have to pay the unnecessary costs that would come with further screening.

## Conclusion

### Limitations

### Next Steps
