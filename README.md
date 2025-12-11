# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the libraries and read the data frame using pandas.
2.Calculate the null values present in the dataset and apply label encoder.
3.Determine test and training data set and apply decison tree regression in dataset.
4.Calculate Mean square error,data prediction and r2.
 
 
 

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: M.Dhanush
RegisterNumber:  25009955

import pandas as pd
data=pd.read_csv("Salary.csv")
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

from sklearn import metrics
mse=metrics.mean_squared_error(y_test, y_pred)
mse

r2=metrics.r2_score(y_test,y_pred)
r2


dt.predict([[5,6]])
*/
```

## Output:
![Decision Tree Regressor Model for Predicting the Salary of the Employee](sam.png)
<img width="574" height="331" alt="Screenshot 2025-12-11 083932" src="https://github.com/user-attachments/assets/18d4296a-3a71-4908-bf32-279e65465fd2" />

<img width="375" height="224" alt="Screenshot 2025-12-11 083940" src="https://github.com/user-attachments/assets/91572ee1-d16d-46db-b2d0-06d64f4c8dab" />


<img width="412" height="136" alt="Screenshot 2025-12-11 083947" src="https://github.com/user-attachments/assets/a8cc2604-7ea1-4c1e-b8c5-9ff778885fee" />


<img width="281" height="35" alt="Screenshot 2025-12-11 083955" src="https://github.com/user-attachments/assets/0c60525a-1b50-43d3-ac00-1f475986fa7f" />

<img width="304" height="42" alt="Screenshot 2025-12-11 084002" src="https://github.com/user-attachments/assets/eb99ba6b-2952-445b-af20-134225b0c186" />

<img width="283" height="42" alt="Screenshot 2025-12-11 084008" src="https://github.com/user-attachments/assets/10ddfee5-b268-4afd-87f4-329440bbb82c" />


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
