# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
Import the required libraries (pandas, numpy, sklearn) and load the dataset

### Step2
Separate the data into independent variables (X, multiple features) and the dependent variable (y), then split into training and testing sets.

### Step3
Create a LinearRegression model and fit it on the training data (model.fit(X_train, y_train)).

### Step4
Print the intercept and coefficients, then predict values for the test set or for new input.

### Step5
Evaluate the model (MSE, R² score) and display the predicted output.

## Program:
```
Developed by: Kishor.M
RegisterNumber: 26018383

import pandas as pd

url = "https://raw.githubusercontent.com/arunpradeep-sec/Linear-Algebra-Lab/main/carsemission.csv"

df = pd.read_csv(url)
df.to_csv("carsemission.csv", index=False)

print("Dataset loaded successfully.")

import pandas as pd

from sklearn import linear_model

df = pd.read_csv("carsemission.csv")

X = df[['Weight', 'Volume']]

y = df['CO2']

regr = linear_model.LinearRegression()

regr.fit(X, y)

print('Coefficients:', regr.coef_)

print('Intercept:', regr.intercept_)

input_data = pd.DataFrame({'Weight': [3300], 'Volume': [1300]})

predictedCO2 = regr.predict(input_data)

print('Predicted CO2 for the corresponding weight and volume:', predictedCO2)


```
## Output:
<img width="1920" height="1080" alt="Screenshot (40)" src="https://github.com/user-attachments/assets/4359d5e7-f977-4337-a2dc-99dc4739c31e" />
<img width="1920" height="1080" alt="Screenshot (41)" src="https://github.com/user-attachments/assets/7d043971-f9c4-4288-876e-acb08001c0ab" />


### Insert your output

<br>

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
