# Bayes-Classifier
## Aim:
To Construct a Bayes Classifier to classiy iris dataset using Python.
## Algorithm:
Input: 
- X: the training data, where each row represents a sample and each column represents a feature.
- y: the target labels for the training data.
- X_test: the testing data, where each row represents a sample and each column represents a feature.

Output:
- y_pred: the predicted labels for the testing data.

1. Create a BayesClassifier class with the following methods:
   a. __init__ method to initialize the Gaussian Naive Bayes classifier from scikit-learn.
   b. fit method to fit the classifier to the training data using the Gaussian Naive Bayes algorithm from scikit-learn.
   c. predict method to make predictions on the testing data using the fitted classifier from scikit-learn.
2. Load the Iris dataset using the load_iris function from scikit-learn.
3. Split the data into training and testing sets using the train_test_split function from scikit-learn.
4. Create a BayesClassifier instance.
5. Train the classifier on the training data using the fit method.
6. Make predictions on the testing data using the predict method.
7. Evaluate the classifier's accuracy using the accuracy_score function from scikit-learn.

## Program:
```
Developed By:M.Harikrishna
Reg.No:212221230059
```
```
import numpy as np
from sklearn.datasets import load_iris
from sklearn.model_selection import train_test_split
from sklearn.naive_bayes import GaussianNB
from sklearn.metrics import accuracy_score
class BayesClassifier:
  def __init__(self):
    self.clf = GaussianNB()
  def fit(self, X, y):
    self.clf.fit(X, y)
  def predict(self, X):
    return self.clf.predict(X)
ir = load_iris()
X_train, X_test, y_train, y_test = train_test_split(ir.data, ir.target,test_size=0.33, random_state = 33)
clf = BayesClassifier()
clf.fit(X_train, y_train)
y_pred = clf.predict(X_test)
accu = accuracy_score(y_test, y_pred)
print("Accuracy:",accu*100)
```

## Output:
<img width="228" alt="image" src="https://github.com/nithin-popuri7/Bayes-Classifier/assets/94154780/1a110c33-7917-461b-9054-2c5a59e06b91">

## Result:
Hence, Bayes classifier for iris dataset is implemented successfully


