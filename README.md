# EX3 Implementation-of-Linear-Regression-Using-Gradient-Descent

## AIM:
To write a program to predict the profit of a city using the linear regression model with gradient descent.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.You are given 4 input data points with 3 features each and a target value (y) for each point.
Initialize:

2.Set theta = [0, 0, 0, 0] (4 coefficients for 3 features + intercept).
Run gradient descent:

3.Calculate predictions, compute errors, and update theta iteratively.
Make Predictions:

4.After finding optimal theta, predict the value for any new data points


## Program:
```
/*
Program to implement the linear regression using gradient descent.
Developed by: A Divya
RegisterNumber:2305002007
import numpy as np
import pandas as pd
from sklearn.preprocessing import StandardScaler
def linear_regression(x1,y,learning_rate=0.01,num_iters=1000):
  X=np.c_[np.ones(len(x1)),x1]
  theta=np.zeros(X.shape[1]).reshape(-1,1)
  for _ in range(num_iters):
    predictions = (X).dot(theta).reshape(-1, 1)
    errors = (predictions - y).reshape(-1, 1)
    theta -= learning_rate * (1 / len(X1)) * X.T.dot(errors)
  return theta
data = pd.read_csv('/content/50_Startups.csv', header=None)
X = (data.iloc[1:, :-2].values)
X1=X.astype(float)
scaler = StandardScaler()
y = (data.iloc[1:,-1].values).reshape(-1,1)
X1_Scaled = scaler.fit_transform(X1)
Y1_Scaled = scaler.fit_transform(y)
theta = linear_regression(X1_Scaled, Y1_Scaled)
new_data = np.array([165349.2,136897.8,471784.1]).reshape(-1,1)
new_Scaled = scaler.fit_transform(new_data)
prediction =np.dot(np.append(1, new_Scaled),theta)
prediction=prediction.reshape(-1,1)
pre=scaler.inverse_transform(prediction)
print(f"Predicted value: {pre}")
*/
```

## Output:
![image](https://github.com/user-attachments/assets/5a33b5d5-caa7-4742-ad85-2447bd397b79)



## Result:
Thus the program to implement the linear regression using gradient descent is written and verified using python programming.
