# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the libraries and read the data frame using pandas.

2.Calculate the null values present in the dataset and apply label encoder.

3.Determine test and training data set and apply decison tree regression in dataset.

4.calculate Mean square error,data prediction and r2.

## Program and Output:
```

Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: HARIHARAN J
RegisterNumber: 212223240047
import pandas as pd
from sklearn.preprocessing import LabelEncoder
from sklearn.model_selection import train_test_split
from sklearn import metrics
from sklearn.tree import DecisionTreeClassifier
data = pd.read_csv("/content/Salary (2).csv")
data.head()
```
![image](https://github.com/user-attachments/assets/356ecaf6-76a7-4257-ad4b-31c3b26157dc)
```
data.info()
```
![image](https://github.com/user-attachments/assets/2eb6a295-9372-4127-b484-d8344e95bbe5)
```
data.isnull().sum()
```
![image](https://github.com/user-attachments/assets/b3dbda9f-b7c1-46f4-831e-8f47dd8f7ef8)
```
le = LabelEncoder()
data["Position"] = le.fit_transform(data["Position"])
data.head()
```
![image](https://github.com/user-attachments/assets/d141ff97-c3da-4fa1-a51b-dee2805745b4)
```
x=data[["Position","Level"]]
y=data[["Salary"]]
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2)
dt.fit(x_train,y_train)dt=DecisionTreeClassifier()
```
![image](https://github.com/user-attachments/assets/9433b554-43b4-49ff-9869-94841c1fb454)
```
y_pred=dt.predict(x_test)
y_pred
```
![image](https://github.com/user-attachments/assets/323739d2-d7d1-4a6f-97ad-302d67ac9f38)
```
mse = metrics.mean_squared_error(y_test, y_pred)
mse 
```
![image](https://github.com/user-attachments/assets/f3b9f8b2-2d32-45bf-b5f7-f1a38095e92b)
```
r2 = metrics.r2_score(y_test, y_pred)
r2
```
![image](https://github.com/user-attachments/assets/f0056866-ee17-4e45-91c4-2aff077e2af7)
```
dt.predict([[5,6]])
```
![image](https://github.com/user-attachments/assets/c058e32f-b58c-4a6b-b1a6-9d324af5bf6b)

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
