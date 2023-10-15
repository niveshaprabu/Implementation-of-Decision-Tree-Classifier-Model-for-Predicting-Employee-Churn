# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn
# AIM:

To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
# Equipments Required:

1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

# Algorithm

1.Import pandas module and import the required data set.

2.Find the null values and count them.

3.Count number of left values.

4.From sklearn import LabelEncoder to convert string values to numerical values.

5.From sklearn.model_selection import train_test_split.

6.Assign the train dataset and test dataset.

7.From sklearn.tree import DecisionTreeClassifier.

8.Use criteria as entropy.

9.From sklearn import metrics. 10.Find the accuracy of our model and predict the require values.
# Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by:Nivesh P
RegisterNumber: 212222040108

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

x=data[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company","Work_accident","promotion_last_5years","salary"]]
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

*/
```
# Output:
# data.head()
![image](https://github.com/niveshaprabu/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/122986499/8589e5ad-99a3-40d2-8e81-17a42d18a20d)

# data.info()
![image](https://github.com/niveshaprabu/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/122986499/994ba2b8-4866-4e66-8efe-b587bc7e498c)

# isnull() and sum ()
![image](https://github.com/niveshaprabu/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/122986499/ac41d533-658f-4325-8534-df9ef3c6debc)

# data value counts()
![image](https://github.com/niveshaprabu/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/122986499/f4152651-6b65-4d5e-b418-25e108db7641)

# data.head() for salary
![image](https://github.com/niveshaprabu/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/122986499/87c7b1e5-35fb-43d4-91ee-69c4b2ceadca)

# x.head()
![image](https://github.com/niveshaprabu/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/122986499/b30b7851-396a-4f5c-a3ac-0dea13da258b)

# accuracy value
![image](https://github.com/niveshaprabu/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/122986499/1d80e138-53d0-4435-9831-29c80256be68)

# data prediction
![image](https://github.com/niveshaprabu/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/122986499/02b424f8-d456-4b76-94ba-dfd58d0cea59)

# Result:
Thus the program to implement the Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
