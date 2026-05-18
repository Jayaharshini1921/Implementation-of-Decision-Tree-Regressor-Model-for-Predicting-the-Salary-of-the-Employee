# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import pandas

2.Import Decision tree classifier

3.Fit the data in the model

4.Find the accuracy score

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Jayaharshini s
RegisterNumber: 212224100024 
*/
```
```
import pandas as pd
data=pd.read_csv("Salary.csv")
data.head()
data.info()
data.isnull().sum()
```
```
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
```
```
x=data[["Position","Level"]]
x.head()
y=data["Salary"]
y.head()

```
```
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)
```

```
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
y_pred
from sklearn.metrics import r2_score
r2=r2_score(y_test,y_pred)
```
```
R2 score:  0.48611111111111116


```
```
dt.predict([[5,6]])
```
## Output:
<img width="958" height="299" alt="390836269-a61bc2cc-84ea-456b-b431-6814e70f21e9" src="https://github.com/user-attachments/assets/d2269a53-e5d5-4211-8797-0222506c465b" />

<img width="399" height="195" alt="390836348-b85ac197-8498-48ee-b61a-e1bfb45397ee" src="https://github.com/user-attachments/assets/f3e653b7-299b-478e-836a-32be65f8f262" />
<img width="697" height="131" alt="390836414-eb0865da-4ded-400b-a133-5bd3868eb59c" src="https://github.com/user-attachments/assets/7a8868ab-c142-4fe0-9c46-c5f86cb09f95" />

<img width="323" height="35" alt="390836467-f2538dc7-b3d6-4927-9403-1ba953b50548" src="https://github.com/user-attachments/assets/ebd06e22-2dd7-4787-b191-2ce875a166ab" />
<img width="200" height="35" alt="390836522-6b53be8b-b5c2-4b09-a220-1ec50aea4747" src="https://github.com/user-attachments/assets/7f3f09e0-4f9d-43c7-b6d7-2c5f7d0dff0f" />

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
