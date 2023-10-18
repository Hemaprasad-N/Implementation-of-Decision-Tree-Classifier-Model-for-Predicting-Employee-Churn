# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.import the required libraries. 
2.Upload and read the dataset. 
3.Check for any null values using the isnull() function. 
4.From sklearn.tree import DecisionTreeClassifier and use criterion as entropy.
5.Find the accuracy of the model and predict the required values by importing the required
module from sklearn.

## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: HEMAPRASAD N
RegisterNumber:  212222040054
*/
```
import pandas as pd
data=pd.read_csv("/content/Employee.csv")
data.head()
data.info()
data.isnull().sum()
data["left"].value_counts()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["salary"]=le.fit_transform(data["salary"])
data.head()
x=data[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time
x.head()
y=data["left"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)
from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
dt.predict([[0.5,0.8,9,260,6,0,1,2]])

## Output:
![decision tree classifier model](sam.png)
![275321069-7d517752-acf3-467d-b3bc-87cfe646e705](https://github.com/Hemaprasad-N/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/135933397/88105402-e05d-4281-913c-7d4e8ffe23f7)
![275321082-abf43f26-9ba0-432c-8dc2-2f70f59a5f94](https://github.com/Hemaprasad-N/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/135933397/6fe3c623-7b84-46a4-8ed0-7ca4670a9f5f)
![275321090-4b51b1b1-2d3b-491e-8c36-70cbffed80df](https://github.com/Hemaprasad-N/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/135933397/6b6bcbba-33fd-4ca5-9819-954b2d3824a6)
![275321093-f3654906-27d2-4ae7-bd48-534e79b40ddb](https://github.com/Hemaprasad-N/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/135933397/727f524c-e8dd-4331-99a5-4bccfd180699)
![275321103-a06a5d4d-1939-4417-9fae-a707a3860057](https://github.com/Hemaprasad-N/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/135933397/4006e4ab-d856-4705-b6ea-23a5d0334eb1)
![275321110-f722f0e0-927a-4795-b9d0-41cc6a79e9ff](https://github.com/Hemaprasad-N/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/135933397/2f5177aa-4e3d-48fe-9481-b520de2a31f4)
![275321130-1fb54cd8-b8ec-40d8-94a3-644a4c3ebe45](https://github.com/Hemaprasad-N/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/135933397/21a7e320-6a30-4d3c-bf40-b6851e1a078f)


## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
