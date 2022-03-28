# credit_risk
Credit risk classification model for peer to peer lending

---

## Technologies

Project uses:

[Pandas](https://pandas.pydata.org/)

[pathlib](https://docs.python.org/3/library/pathlib.html)

[numpy](https://numpy.org/)

[SKLearn](https://scikit-learn.org/stable/)

[IMBlearn](https://imbalanced-learn.org/stable/install.html)




---

## Installation Guide

Run this program in Jupyter notebook and have IMBLearn, pandas, SKlearn, numpy and path installed



---

## Usage

Utilize Jupyter Labs to interact with the software program

!["Jupyter Labs Example"](https://miro.medium.com/max/955/1*mXGu0MeYgnUkyR9ybVlQpg.png)

**Key example code for model creation**
```
# Instantiate the Logistic Regression model
# Assign a random_state parameter of 1 to the model
model = LogisticRegression(random_state=1)

# Fit the model using the resampled training data
lr_resampled_model = model.fit(X_resampled, y_resampled)
lr_resampled_model

# Make a prediction using the testing data
y_resampled_pred = lr_resampled_model.predict(X_test)
```
## Results

* Machine Learning Model 1: "Original"
  * Model 1 uses factors including Loan Size, Interest Rate, Borrower Income, Debt to Income Ratio, Number of Accounts, Deragtory Marks, and Total Debt to predict credit risk for a loan using a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.
  Model 1 Stats:
  Balanced Accuracy Score: .9520
  Confusion Matrix: 
       [18663,   102]
       [   56,   563]




* Machine Learning Model 2: "Resampled"
  * Model 2 uses the same factors as Model 1, and leverages the same initial dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers. However, the data set has imbalanced classes of data because healthy loans outnumber risky loans. For this reason, Model 2 resamples the data to more effectively predict credit risk. 
  Model 1 Stats:
  Balanced Accuracy Score: .9936
  Confusion Matrix: 
       [18663,   116]
       [    4,   615]

## Summary

* The resampled regression model appears to be superior to the original with a higher balanced accuracy score which more accurately predicts credit risk in borrowers by lowering the number of false negatives.
* In this scenario, it is important to be able to more accurately identify risky borrowers. The model performance depends on the problem we are trying to solve because false negatives (a credit risk assesment that fails to identify a risky borrower causes a larger negative financial impact than a false positive (Where a healthy borrower is mis-identified as high risk)
---

## Contributors

Hugo Kostelni

---

## License

Open Source

