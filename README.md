# Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student

## AIM:

To write a program to implement the the Logistic Regression Model to Predict the Placement Status of Student.

## Equipments Required:

1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

 1.Use the standard libraries in python for finding linear regression.
 
2.Set variables for assigning dataset values.

3.Import linear regression from sklearn.

4.Predict the values of array.

5.Calculate the accuracy, confusion and classification report by importing the required modules from sklearn.

6.Obtain the graph.

## Program:

```/*
Program to implement the the Logistic Regression Model to Predict the Placement Status of Student.
Developed by:Hemavathi.N 
RegisterNumber: 212221040055

import pandas as pd
data=pd.read_csv('/content/Placement_Data (1).csv')
print("Placement data")
data.head()

data1=data.copy()
data1=data1.drop(["sl_no","salary"],axis=1)
print("Salary data")
data1.head()

print("Checking the null() function")
data1.isnull().sum()

print("Data Duplicate")
data1.duplicated().sum()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data1["gender"]=le.fit_transform(data1["gender"])
data1["ssc_b"]=le.fit_transform(data1["ssc_b"])
data1["hsc_b"]=le.fit_transform(data1["hsc_b"])
data1["hsc_s"]=le.fit_transform(data1["hsc_s"])
data1["degree_t"]=le.fit_transform(data1["degree_t"])
data1["workex"]=le.fit_transform(data1["workex"])
data1["specialisation"]=le.fit_transform(data1["specialisation"])
data1["status"]=le.fit_transform(data1["status"])
print("Print data")
data1

x=data1.iloc[:,:-1]
print("Data-status")
x

y=data1["status"]
print("data-status")
y


from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)

from sklearn.linear_model import LogisticRegression
lr=LogisticRegression(solver="liblinear")
lr.fit(x_train,y_train)
y_pred=lr.predict(x_test)
print("y_prediction array")
y_pred

from sklearn.metrics import accuracy_score
accuracy=accuracy_score(y_test,y_pred)
print("Accuracy value")
accuracy

from sklearn.metrics import confusion_matrix
confusion = confusion_matrix(y_test,y_pred)
print("Confusion array")
confusion

from sklearn.metrics import classification_report
classification_report1 = classification_report(y_test,y_pred)
print("Classification report")
print(classification_report1)

print("Prediction of LR")
lr.predict([[1,80,1,90,1,1,90,1,0,85,1,85]])
![image](https://github.com/212221040055/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/128135323/f840fc3e-d52b-4ab1-8c17-033fa14ae612)

![Screenshot 2023-05-19 133221](https://github.com/212221040055/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/128135323/e5fe8817-dde4-4a5c-9b60-6b408ae32edd)
![Screenshot 2023-05-19 133241](https://github.com/212221040055/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/128135323/913da82a-3c86-4704-b19c-4fdf1e1482c3)
![Screenshot 2023-05-19 133301](https://github.com/212221040055/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/128135323/f92ad1c5-aab5-453c-b874-bd1e7e183e9c)
![Screenshot 2023-05-19 133331](https://github.com/212221040055/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/128135323/b6ee2fc6-5301-43b5-9ad0-a4089e48209f)
![Screenshot 2023-05-19 133221](https://github.com/212221040055/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/128135323/99c4abd9-fda7-4f8a-9da6-973c6a73129d)

## Result:

Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.
