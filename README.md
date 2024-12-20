# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import essential libraries like pandas, numpy, and sklearn. Load the dataset containing employee features (e.g., experience, education) and the target (salary).
2. Handle missing values, encode categorical features (e.g., department) using OneHotEncoder or LabelEncoder. Normalize or scale numerical features if necessary to ensure consistent data for the model.
3. Use train_test_split() from sklearn.model_selection to divide the data into training and testing sets. Typically, you split the data into 80% for training and 20% for testing.
4. Use DecisionTreeRegressor from sklearn.tree and fit the model on the training data. You can specify parameters such as max_depth or min_samples_split to control the complexity of the tree.
5. Use the trained model to predict the salary for the employees in the test dataset. Store these predictions and compare them with the actual salaries for evaluation.
6. Use regression evaluation metrics like mean_squared_error, r2_score, or mean_absolute_error from sklearn.metrics. These metrics will help assess how well the model predicts employee salaries.
7. Use plot_tree() from sklearn.tree to visualize the structure of the decision tree. This will give insights into the most important features influencing salary predictions and how the tree splits.
 
## Program:

```
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: T.Roshini
RegisterNumber: 212223230175

import pandas as pd
data = pd.read_csv("Salary.csv")
data.head()
data.info()
data.isnull.sum()
data["Salary"].value_counts()
from sklearn.preprocessing import LabelEncoder 
le = LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
x=data[["Position","Level"]]
x.head()
y=data[["Salary"]]
y.head()
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test = train_test_split(x,y,test_size = 0.2, random_state = 2)
from sklearn.tree import DecisionTreeRegressor
dt = DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred = dt.predict(x_test)
from sklearn import metrics
mse = metrics.mean_squared_error(y_test,y_pred)
mse
r2 = metrics.r2_score(y_test,y_pred)
r2
dt.predict([[5,6]])

```

## Output:

#### Dataset

 ![369341984-9ccf8cfb-a6aa-4e60-8f71-ca44b768829c](https://github.com/user-attachments/assets/687fdbd0-e5d6-4f30-b4dd-e471d0b9a0ab)

#### Data Info
 
 ![369342103-b759ddef-343d-4e92-b7a4-0450ea778868](https://github.com/user-attachments/assets/125e3a97-7398-4ae6-a597-a84b3e1ba3f8)

#### Sum of Null Values

 ![369342145-c321c4a7-240d-4761-bec9-6a7d5bd1fc8d](https://github.com/user-attachments/assets/f8739202-af9c-4c40-aa33-4a007d67d687)

#### Value count of Salary column in data set

 ![369342300-d61db949-3393-419b-9df3-50571dca51e4](https://github.com/user-attachments/assets/c10839de-e6f7-477c-99a6-a1d53bfd75fe)

#### Labelling Position column
 
 ![369342483-75b61a3c-8135-438a-96b3-87ab522cc0ff](https://github.com/user-attachments/assets/291c9435-b9f9-4250-8178-c2488e92aa5d)

#### Assigning x and y value

 ![369342646-d2bc234b-8598-4a8a-ab44-5ae78bfb0ccd](https://github.com/user-attachments/assets/eea076eb-40ae-463e-be98-5aefad4f8e5d)
 ![369342679-4a768e02-6e41-4b11-afaf-4700e12fb21c](https://github.com/user-attachments/assets/53448b1f-af21-422c-916f-49a793e632a4)

#### Mean Squared Error

 ![369342863-2255737d-d993-45d7-b49b-fab332b209a5](https://github.com/user-attachments/assets/de2225af-a82f-42f5-9f16-2bbce0749103)

#### R2

 ![369342948-6514ee73-81de-411e-ba94-c38b1f07b1f2](https://github.com/user-attachments/assets/8a1379ff-416b-4f44-893d-55d910da1f1a)

#### Prediction

 ![369343064-d991d972-0728-4042-a1e4-711351309ee2](https://github.com/user-attachments/assets/3f2c1233-b52d-4c19-969b-c5a797f03f18)

## Result:

Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
