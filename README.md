# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import standard libraries in python for finding Decision tree regressor model for predicting the
salary of the employee.
2. Initialize and print the Data.head(),data.info(),data.isnull().sum()
3. Visualize data value count.
4. Import sklearn from LabelEncoder.
5. Split data into training and testing.  
6. Calculate the MSE Value,r2 Value and  data prediction by importing the required modules from sklearn

## Program:
```txt
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Suriya Prakash B
RegisterNumber:  212220220048
```
```py3
import pandas as pd
data=pd.read_csv("/content/Salary.csv")
print("Data.head():")
data.head()
```
```py3
print("Data.info():")
data.info()
```
```py3
print("Data.isnull() and Sum():")
data.isnull().sum()
```
```py3
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
print("data.head() for Salary:")
data["Position"]=le.fit_transform(data["Position"])
data.head()
```
```py3
x=data[["Position","Level"]]
y=data[["Salary"]]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)
```
```py3
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
print("MSE Value:")
from sklearn import metrics
mse=metrics.mean_squared_error(y_test,y_pred)
mse
```
```py3
print("r2 Value:")
r2=metrics.r2_score(y_test,y_pred)
r2
```
```py3
print("data prediction:")
dt.predict([[5,6]])
```

## Output:
![image](https://github.com/Yugendaran/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/128135616/a5c75a84-b0fb-44a7-8b0d-71ec1dd39ef5)<br>
![image](https://github.com/Yugendaran/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/128135616/a53c9b52-b6ea-4ce8-a357-acd1be6f5531)<br>
![image](https://github.com/Yugendaran/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/128135616/c9e9e5e6-0fe7-4fa9-8fc8-3c769a05b527)<br>
![image](https://github.com/Yugendaran/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/128135616/fbd18426-6def-486b-985d-0fd866fd215e)<br>
![image](https://github.com/Yugendaran/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/128135616/a44b6e1c-cb3b-4dae-a09a-56c65ea72a67)<br>
![image](https://github.com/Yugendaran/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/128135616/2468c5e6-89b2-4108-9e27-b6efc9ef597d)<br>
![image](https://github.com/Yugendaran/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/128135616/b5eb9829-f8fe-483d-9c60-268947ceafb3)<br>

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
