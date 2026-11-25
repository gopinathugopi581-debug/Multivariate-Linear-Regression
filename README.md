# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1: Start and import the required libraries.

### Step2: Step 2: Enter the input features and target values, then separate them into \(X\) and \(y\).

### Step3: Add a column of ones to \(X\) for the intercept and initialize the model coefficients.

### Step4: Train the model using gradient descent: calculate predictions and errors, then update the coefficien

### Step5:  Use the trained model to predict the output for new input values, display the result, and stop.

## Program:
```
name:Gopinath n
ref no:26007691
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
<img width="1498" height="627" alt="image" src="https://github.com/user-attachments/assets/61561bb5-5517-4568-b333-17a31463bde0" />
<img width="1326" height="166" alt="image" src="https://github.com/user-attachments/assets/55acf6bf-abbc-49dc-9734-0f227cc7a4a8" />


## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
