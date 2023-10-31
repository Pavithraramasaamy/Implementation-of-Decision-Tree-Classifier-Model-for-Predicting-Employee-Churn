# EX-06-Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

  1. Import pandas module and import the required data set.

  2. Find the null values and count them.

  3. Count number of left values.

  4. From sklearn import LabelEncoder to convert string values to numerical values.

  5.From sklearn.model_selection import train_test_split.

  6.From sklearn import metrics.Find the accuracy of our model and predict the require values.

## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: PAVITHRA R
RegisterNumber:  212222230106

import pandas as pd
data = pd.read_csv("/content/Employee.csv")
data.head()
data.info()

data.isnull().sum()

data["left"].value_counts

from sklearn.preprocessing import LabelEncoder
le= LabelEncoder()
data["salary"]=le.fit_transform(data["salary"])
data.head()

x= data[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company","Work_accident","promotion_last_5years","salary"]]

x.head()
y=data["left"]

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test = train_test_split(x,y,test_size=0.2,random_state = 100)


from sklearn.tree import DecisionTreeClassifier
dt = DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)

y_pred = dt.predict(x_test)
from sklearn import metrics

accuracy = metrics.accuracy_score(y_test,y_pred)
accuracy

dt.predict([[0.5,0.8,9,260,6,0,1,2]])
*/
```

## Output:

## 1.DATASET:

![1](https://github.com/Pavithraramasaamy/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118596964/f9a48059-788c-452d-99ea-7c6912c58879)


## 2.df.head()

![2](https://github.com/Pavithraramasaamy/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118596964/e56e6ab3-5109-4a5a-b7f4-c054b5e4c842)

## 3.df.inf0()

![3](https://github.com/Pavithraramasaamy/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118596964/aa91cd86-7e5a-4a00-ba3d-28fe986d03ed)

## 4.ISNULL:

![4](https://github.com/Pavithraramasaamy/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118596964/67393d0e-0616-4d30-b63b-57a14dd08db8)


## 5.VALUE COUNTS:

![5](https://github.com/Pavithraramasaamy/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118596964/40da44a1-40df-49e4-a81e-288407bc67dc)

## 6.Dataset transformed head:

![239680850-d5154e3f-27f1-4bc7-b003-d815bb6cb98f](https://github.com/Pavithraramasaamy/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118596964/214bebaa-fcac-4a6f-bdb8-9bfc28ba9ab6)



## 7.X.head():

![6](https://github.com/Pavithraramasaamy/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118596964/001c3d06-e203-442b-9c3e-1c43dbc269dc)


## 8.DECISION TREE:

![7](https://github.com/Pavithraramasaamy/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118596964/73c0555e-2c75-40c0-86ea-1a69c60c4aed)


## 9.ACCURACY:

![8](https://github.com/Pavithraramasaamy/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118596964/d90e7c59-cc85-4dcb-b574-7fe1b58b9703)


## 10.PREDICT:

![9](https://github.com/Pavithraramasaamy/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118596964/e275dca9-0f6a-4944-97fe-b359c993582e)



## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
