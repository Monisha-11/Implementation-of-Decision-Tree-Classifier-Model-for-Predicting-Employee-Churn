# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm

### STEP 1:

Import pandas library to read csv or excel file.

### STEP 2:

Import LabelEncoder using sklearn.preprocessing library.

### STEP 3:

Transform the data's using LabelEncoder.

### STEP 4:

Import decision tree classifier from sklearn.tree library to predict the values.

### STEP 5:

Find accuracy and Predict the values.
End of the program.

## Program:
```python

Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: Monisha T
RegisterNumber:  212221240029

import pandas as pd
data=pd.read_csv("Employee.csv")
data.head()
data.info()
data.isnull().sum()
data["left"].value_counts()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["salary"]=le.fit_transform(data["salary"])
data.head()
X=data[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company","Work_accident","promotion_last_5years","salary"]]
X.head()
Y=data["left"]
from sklearn.model_selection import train_test_split
X_train,X_test,Y_train,Y_test=train_test_split(X,Y,test_size=0.2,random_state=100)
from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion="entropy")
dt.fit(X_train,Y_train)
Y_pred=dt.predict(X_test)
from sklearn import metrics
accuracy=metrics.accuracy_score(Y_test,Y_pred)
accuracy
dt.predict([[0.5,0.8,9,260,6,0,1,2]])

```

# Output:

## DATA HEAD:

![output](./output1.png)

## DATA INFO:

![output](./output2.png)

## DATA ISNULL:

![output](./output3.png)

## DATA LEFT:

![output](./output4.png)

## DATA HEAD:
![output](./output5.png)

## X.HEAD:
![output](./output6.png)

## dt.FIT:

![output](./output7.png)

## ACCURACY
![output](./output8.png)

## dt.PREDICT
![output](./output9.png)


## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
