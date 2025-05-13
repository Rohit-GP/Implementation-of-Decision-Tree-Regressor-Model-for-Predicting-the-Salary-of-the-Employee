# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import pandas
2. Import Decision tree classifier
3. Fit the data in the model
4. Find the accuracy score

## Program:

Name : Rohit GP

Ref/Reg No : 24900185 / 212224220082
```
import pandas as pd
data=pd.read_csv(r"/content/Salary.csv")
data
```
```
data.head()
data.info()
data.isnull().sum()
```
```
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
print(data.head())
```
```
x=data[["Position","Level"]]
print(x.head())
```
```
y=data["Salary"]
y.head()
```
```
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)

from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
print(y_pred)
```
```
from sklearn import metrics
r2=metrics.r2_score(y_test,y_pred)
print(r2)
```
```
dt.predict([[5,6]])
```

## Output:

![image](https://github.com/user-attachments/assets/c0a462e9-ccae-4436-9173-a6a64f591a1e)

![image](https://github.com/user-attachments/assets/66ea1dbb-6a4b-4902-b605-fc8e27ca5e7b)

![image](https://github.com/user-attachments/assets/8aca6cb4-1837-4402-b336-d523cbd828fd)

![image](https://github.com/user-attachments/assets/8d42a18a-f9b0-47de-8dd6-62e625e7f51c)

![image](https://github.com/user-attachments/assets/f6bfe4c1-cd7d-4203-aa58-a97db0ddf6ae)

![image](https://github.com/user-attachments/assets/44c031e6-ed42-43bc-bac7-86a195b3ecaf)

![image](https://github.com/user-attachments/assets/079fc718-f47c-4eb5-b7bb-e8c274af2281)

![image](https://github.com/user-attachments/assets/08429101-8f7b-4f83-b03a-a4798fa918f1)


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
