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
Developed by: HARSHINI.V
RegisterNumber:  212224040109
*/
```
 import pandas as pd
 
 
 data=pd.read_csv("/Salary.csv")

 
 data.head()
 
 
 data.info()

 
 data.isnull().sum()
 
 
 from sklearn.preprocessing import LabelEncoder
 
 
 le=LabelEncoder()
 
 
 data["Position"]=le.fit_transform(data["Position"])
 
 
 data.head()
 
 
 x=data[["Position","Level"]]

 
 x.head()

 
 y=data["Salary"]
 
 
 y.head()
 
 
 from sklearn.model_selection import train_test_split
 
 
 x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)

 
 from sklearn.tree import DecisionTreeRegressor
 
 
 dt=DecisionTreeRegressor()
 
 
 dt.fit(x_train,y_train)

 
 y_pred=dt.predict(x_test)
 
 
 y_pred
 
 
 r2=metrics.r2_score(y_test,y_pred)
 
 
 r2


dt.predict([[5,6]])

## Output:



![image](https://github.com/user-attachments/assets/27e18c98-d686-446a-804e-3cdc6a180811)




![image](https://github.com/user-attachments/assets/22d97532-eaa5-4224-abe5-c9f83d26281b)




## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
