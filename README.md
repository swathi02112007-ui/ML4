# SGD-Regressor-for-Multivariate-Linear-Regression

## AIM:
To write a program to predict the price of the house and number of occupants in the house with SGD regressor.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

1. Import Libraries
Import required Python libraries: numpy, pandas, sklearn.

2. Load Dataset
Load or create a dataset with features (e.g., area, number of rooms, location index).

Include target variables (house price, number of occupants).

3. Preprocess Data
Handle missing values if present.

Scale features using StandardScaler to speed up convergence.

4. Split Dataset
Use train_test_split to split data into training and testing sets.

5. Train Model with SGD Regressor
Initialize SGDRegressor with a learning rate and max iterations.

Use MultiOutputRegressor for predicting multiple outputs.

Train model using the training set.

6. Make Predictions
Predict house price and number of occupants for the test set.

7. Evaluate Model
Use metrics such as r2_score and mean_squared_error to check performance.

8. Display Results
Print actual vs predicted values for better understanding.

## Program:
```
/*
Program to implement the multivariate linear regression model for predicting the price of the house and number of occupants in the house with SGD regressor.

# Ex:No 4
#Manual Implementation using Numpy
import numpy as np

# ------------------------------
# Step 1: Sample dataset
# ------------------------------
# Features: [Hours Studied, Attendance, Previous Marks]
# Features and target
X = np.array([
    [2, 80, 50],
    [3, 60, 40],
    [5, 90, 70],
    [7, 85, 80],
    [9, 95, 90]
])
# Target: Marks Scored
y = np.array([50, 45, 70, 80, 95])

#Using scikit-learn SGDRegressor
from sklearn.model_selection import train_test_split
from sklearn.linear_model import SGDRegressor
from sklearn.preprocessing import StandardScaler
from sklearn.metrics import r2_score, mean_squared_error

# Features and target
X = np.array([
    [2, 80, 50],
    [3, 60, 40],
    [5, 90, 70],
    [7, 85, 80],
    [9, 95, 90]
])
y = np.array([50, 45, 70, 80, 95])

# Split of Dataset
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.25, random_state=42
)

# Feature scaling
scaler = StandardScaler()
X_train = scaler.fit_transform(X_train)
X_test = scaler.transform(X_test)

# Create SGD Regressor
sgd_reg = SGDRegressor(max_iter=1000, learning_rate='invscaling', eta0=0.01, random_state=42)
sgd_reg.fit(X_train, y_train)

# Predictions
y_pred = sgd_reg.predict(X_test)

# Evaluation
print("R2 Score:", r2_score(y_test, y_pred))
print("\nMSE:", mean_squared_error(y_test, y_pred))

# Coefficients and intercept
print("\nWeights (coefficients):", sgd_reg.coef_)
print("\nIntercept:", sgd_reg.intercept_)

# Predict all values
all_pred = sgd_reg.predict(scaler.transform(X))
print("\nPredicted values:", all_pred)

Developed by: Swathi P N
RegisterNumber:  212225230279
*/
```

## Output:

![alt text](ml4.1.png)

![alt text](ml4.2.png)

![alt text](<ml4.3 (2).png>)


## Result:
Thus the program to implement the multivariate linear regression model for predicting the price of the house and number of occupants in the house with SGD regressor is written and verified using python programming.
