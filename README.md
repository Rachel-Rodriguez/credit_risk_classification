# credit_risk_classification

#  Background


In this Challenge various techniques were used to train and evaluate a model based on loan risk. The dataset consists of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

#  Instructions


1. Split the Data into Training and Testing Sets


-  Read the lending_data.csv data from the Resources folder into a Pandas DataFrame.

-  Create the labels set (y) from the “loan_status” column, and then create the features (X) DataFrame from the remaining columns.

NOTE
A value of 0 in the “loan_status” column means that the loan is healthy. A value of 1 means that the loan has a high risk of defaulting.

- Split the data into training and testing datasets by using train_test_split.

2. Create a Logistic Regression Model with the Original Data


- Fit a logistic regression model by using the training data (X_train and y_train).

- Save the predictions for the testing data labels by using the testing feature data (X_test) and the fitted model.

Evaluate the model’s performance by doing the following:

- Generate a confusion matrix.

- Print the classification report.

Answer the following question: How well does the logistic regression model predict both the 0 (healthy loan) and 1 (high-risk loan) labels?

#  Results

The logistic regression model was 95% accurate according to the balanced accuracy score. 
![pic one](https://github.com/Rachel-Rodriguez/credit_risk_classification/assets/124642442/cbd73c15-2b64-4039-88f3-c1f4cb54ba1d)

However, the confusion matrix shows that the data is very imbalanced. There are a lot more healthy loans than there are high risk loans.
![Pic 2](https://github.com/Rachel-Rodriguez/credit_risk_classification/assets/124642442/4035949f-a855-492d-ac33-7b2cc953b38d)

The classification report reveals that the model is 100% accurate predicting healthy loans but only 85% accurate when predicting high-risk loans.
![Pic 3](https://github.com/Rachel-Rodriguez/credit_risk_classification/assets/124642442/98eec836-dcdc-46d9-b185-1ee1301f36cd)

To rectify this issue, a random over-sampler was used in the next iteration of the model.
![pic 4](https://github.com/Rachel-Rodriguez/credit_risk_classification/assets/124642442/364509a4-9bae-417f-a211-ce9f453c1b2a)

The model fit with oversampled data was 99% accurate as opposed to 95% previously.
![pic 5](https://github.com/Rachel-Rodriguez/credit_risk_classification/assets/124642442/8dfbeebf-e298-42c9-b349-a8afe0ce79d1)

The oversampled model seems to be better at correctly classifying high risk loans as evidenced by the recall score which was originally 0.91, now 0.99.
![pic 6](https://github.com/Rachel-Rodriguez/credit_risk_classification/assets/124642442/14e8c388-2c8f-415d-9d8c-f4bfca3890ed)
![pic 7](https://github.com/Rachel-Rodriguez/credit_risk_classification/assets/124642442/d884ab9e-840c-4eac-a33f-75dc4ffaab32)
![pic 8](https://github.com/Rachel-Rodriguez/credit_risk_classification/assets/124642442/e48efaee-d2a3-4d0a-9316-743155d46dbe)


