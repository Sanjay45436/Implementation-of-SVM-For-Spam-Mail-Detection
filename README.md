# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import required libraries (pandas, chardet, sklearn, etc.).

2.Detect the encoding of the CSV file using chardet.

3.Read the CSV file with the correct encoding.

4.Check the data for structure and missing values.

5.Split the data into input (x = messages) and output (y = labels).

6.Divide the data into training and testing sets.

7.Convert text data into numbers using CountVectorizer.

8.Train an SVM model, make predictions, and calculate accuracy.

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: SANJAY S
RegisterNumber: 212225040374

import chardet
file='spam.csv'
with open(file,'rb')as rawdata:
    result=chardet.detect(rawdata.read(100000))
result

import pandas as pd
data=pd.read_csv("spam.csv",encoding='windows-1252')
data.head()

data.info()

data.isnull().sum()

x=data["v2"].values
y=data["v1"].values
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)

from sklearn.feature_extraction.text import CountVectorizer
cv=CountVectorizer()
x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)

from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)
y_pred=svc.predict(x_test)
y_pred

from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy 
*/
```

## Output:
Result output:
<img width="1243" height="38" alt="image" src="https://github.com/user-attachments/assets/9a529d5c-95c2-4e13-bb97-322a752629b4" />

data.head():
<img width="1243" height="227" alt="image" src="https://github.com/user-attachments/assets/0c2b4d53-79ea-4a0c-9db8-63414c679f52" />

data.info():
<img width="1231" height="257" alt="image" src="https://github.com/user-attachments/assets/839606f0-ed6f-4800-a22e-21d40693eec7" />

data.isnull().sum():
<img width="1231" height="130" alt="image" src="https://github.com/user-attachments/assets/2ca15b5b-e2f0-4717-8e00-90e739e41480" />

y_pred:
<img width="1243" height="37" alt="image" src="https://github.com/user-attachments/assets/2809559e-f06c-45dc-9e56-fe67325acc54" />

accuracy():
<img width="1243" height="38" alt="image" src="https://github.com/user-attachments/assets/6334f2e5-6c48-4051-a345-5d966625c02a" />

## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
