# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import pandas as pd and import the required dataset.
2. Calculate the null values in the dataset.
3. Import the LabelEncoder from sklearn.preprocessing
4. Convert the string values to numeric values.
5. Import train_test_split from sklearn.model_selection.
6. Assign the train and test dataset.
7. Import DecisionTreeRegressor from sklearn.tree.
8. Import metrics from sklearn.metrics.
9. Calculate the MeanSquareError.
10. Apply the metrics to the dataset.
11. Predict the output for the required values.
 
## Program:
```
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: T.Roshini
RegisterNumber: 212223230175
```
```
import pandas as pd
data=pd.read_csv("C:/Users/admin/Downloads/Salary.csv")
data.head()
```
```
data.info()
```
```
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
y=data["Salary"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
mse=metrics.mean_squared_error(y_test,y_pred)
mse
```
```
r2=metrics.r2_score(y_test,y_pred)
r2
```
```
dt.predict([[5,6]])
```
## Output:

![Screenshot 2024-10-15 204310](https://github.com/user-attachments/assets/51155bf6-2715-4351-9680-d7f2ca8c7282)

![Screenshot 2024-10-15 204316](https://github.com/user-attachments/assets/9cf5c296-5b23-4647-a0dc-d1fd2d564482)

![Screenshot 2024-10-15 204323](https://github.com/user-attachments/assets/81c12219-d063-4b81-84a9-40578d1d9cb1)

![Screenshot 2024-10-15 204329](https://github.com/user-attachments/assets/952b2352-ac17-41b1-9f99-3fbea0537597)

![Screenshot 2024-10-15 204334](https://github.com/user-attachments/assets/8b2f2f83-495f-49bc-945b-3d868a084b10)

![Screenshot 2024-10-15 204340](https://github.com/user-attachments/assets/098f6efe-12c2-4c47-a9a7-ec4c20305bfb)

![Screenshot 2024-10-15 204346](https://github.com/user-attachments/assets/6939133a-81ce-4b87-af8c-de59842ebb8d)

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
