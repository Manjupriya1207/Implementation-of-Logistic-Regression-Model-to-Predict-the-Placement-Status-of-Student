# Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student

## AIM:
To write a program to implement the the Logistic Regression Model to Predict the Placement Status of Student.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm:
1.Import the standard libraries.

2.Upload the dataset and check for any null or duplicated values using .isnull() and .duplicated() function respectively.

3.Import LabelEncoder and encode the dataset.

4.Import LogisticRegression from sklearn and apply the model on the dataset.

5.Predict the values of array.

6.Calculate the accuracy, confusion and classification report by importing the required modules from sklearn.

7.Apply new unknown values.




## Program:
```
/*
Program to implement the the Logistic Regression Model to Predict the Placement Status of Student.
Developed by: Manjupriya P
RegisterNumber:  212220220024
*/
```
import pandas as pd data = pd.read_csv("Placement_Data.csv") data.head()

data1 = data.copy() data1 = data1.drop(["sl_no","salary"],axis = 1) data1.head()

data1.isnull().sum()

data1.duplicated().sum()

from sklearn.preprocessing import LabelEncoder le = LabelEncoder() data1["gender"] = le.fit_transform(data1["gender"]) data1["ssc_b"] = le.fit_transform(data1["ssc_b"]) data1["hsc_b"] = le.fit_transform(data1["hsc_b"]) data1["hsc_s"] = le.fit_transform(data1["hsc_s"]) data1["degree_t"] = le.fit_transform(data1["degree_t"]) data1["workex"] = le.fit_transform(data1["workex"]) data1["specialisation"] = le.fit_transform(data1["specialisation"]) data1["status"] = le.fit_transform(data1["status"]) data1

x = data1.iloc[:,:-1] x

y = data1["status"] y

from sklearn.model_selection import train_test_split x_train,x_test,y_train,y_test = train_test_split(x,y,test_size = 0.2,random_state = 0)

from sklearn.linear_model import LogisticRegression lr = LogisticRegression(solver = "liblinear") lr.fit(x_train,y_train)

y_pred = lr.predict(x_test) y_pred

from sklearn.metrics import accuracy_score accuracy = accuracy_score(y_test,y_pred) accuracy

from sklearn.metrics import confusion_matrix confusion = confusion_matrix(y_test,y_pred) confusion

from sklearn.metrics import classification_report classification_report1 = classification_report(y_test,y_pred) classification_report1

lr.predict([[1,80,1,90,1,1,90,1,0,85,1,85]])

## Output:
1.Placement data
![Screenshot (24)](https://github.com/Manjupriya1207/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/113583090/62e0f6f1-1e2c-4231-b418-42d00b017ce2)
2.Salary data
![Screenshot (25)](https://github.com/Manjupriya1207/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/113583090/0c234291-7cdd-4c81-98e7-e08d9f7ee31d)
3.Checking the null() function
![Screenshot (26)](https://github.com/Manjupriya1207/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/113583090/b19d6063-345c-4e66-869f-c815473e14c2)
4.Data Duplicate
![Screenshot (27)](https://github.com/Manjupriya1207/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/113583090/828c2061-e6d9-4593-ac62-c96c6e2ed2fc)
5.Print data
![Screenshot (28)](https://github.com/Manjupriya1207/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/113583090/44f2fea2-ad0a-4da8-b9b5-49452eb79dcc)
6.Data-status
![Screenshot (29)](https://github.com/Manjupriya1207/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/113583090/cd5b41c2-1bc3-4029-8986-b218b084290d)
![Screenshot (30)](https://github.com/Manjupriya1207/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/113583090/db026c4a-0c98-4e26-8095-d438594ea104)
7.y_prediction array
![Screenshot (31)](https://github.com/Manjupriya1207/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/113583090/5b3f79f9-f5c0-479c-bced-5e5047491198)
8.Accuracy value
![Screenshot (32)](https://github.com/Manjupriya1207/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/113583090/6fb154e0-8531-40a6-a023-bfd84f46b784)
9.Confusion array
![Screenshot (33)](https://github.com/Manjupriya1207/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/113583090/805f1bed-afa1-48b7-8be8-6f651333b122)
10.Classification report
![Screenshot (34)](https://github.com/Manjupriya1207/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/113583090/d6cac8a6-ba07-49c7-a8db-a6a4dc49dacc)

11.Prediction of LR
![Screenshot (35)](https://github.com/Manjupriya1207/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/113583090/419e4f38-ae73-480b-845b-3a0b50779101)




## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.
