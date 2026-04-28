# Implementation-of-Linear-Regression-Using-Gradient-Descent

## AIM:
To write a program to predict the profit of a city using the linear regression model with gradient descent.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula.
4. <img width="231" height="100" alt="583965822-99f10441-22da-425d-a0ba-e4b6621b1cc9" src="https://github.com/user-attachments/assets/8b5fa0f3-2137-4bf7-8d7e-75170073b73d" />
5. Compute the y -intercept of the line by using the formula:
<img width="295" height="79" alt="image" src="https://github.com/user-attachments/assets/db3215b1-b672-48cd-9a2c-86ee28ad0b4c" />
6. Use the slope m and the y -intercept to form the equation of the line.
7. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```
/*
# Program to implement Linear Regression using Gradient Descent
# Developed by: Iswarya S
# Register Number: 212225040135

# Step 1: Import Libraries
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

# Step 2: Create Dataset (Hours studied vs Marks scored)
data = {
    "Hours_Studied": [1, 2, 3, 4, 5, 6, 7, 8, 9, 10],
    "Marks_Scored":  [35, 40, 50, 55, 60, 65, 70, 80, 85, 95]
}

df = pd.DataFrame(data)

# Display dataset
print("Dataset:\n", df)

# Step 3: Define Variables
X = np.array(df["Hours_Studied"])
y = np.array(df["Marks_Scored"])

# Step 4: Initialize Parameters
m = 0   # Slope
b = 0   # Intercept

learning_rate = 0.01
epochs = 1000
n = len(X)

# Step 5: Gradient Descent Algorithm
for i in range(epochs):

    # Predicted values
    y_pred = m * X + b

    # Calculate gradients
    dm = (-2/n) * sum(X * (y - y_pred))
    db = (-2/n) * sum(y - y_pred)

    # Update parameters
    m = m - learning_rate * dm
    b = b - learning_rate * db

# Step 6: Print Model Parameters
print("\nModel Parameters:")
print("Slope (m):", m)
print("Intercept (b):", b)

# Step 7: Predictions
predictions = m * X + b

# Step 8: Visualization
plt.figure(figsize=(8,6))
plt.scatter(X, y, label="Actual Data")
plt.plot(X, predictions, linewidth=2, label="Regression Line")
plt.xlabel("Hours Studied")
plt.ylabel("Marks Scored")
plt.title("Linear Regression using Gradient Descent")
plt.legend()
plt.grid(True)
plt.show()

# Step 9: Predict for custom input
hours = float(input("Enter study hours: "))

predicted_marks = m * hours + b

print(f"Predicted marks for {hours} hours = {predicted_marks:.2f}")
*/
```

## Output:
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/135b0bfb-4fa4-4ff9-8927-385dec1b5346" />


## Result:
Thus the program to implement the linear regression using gradient descent is written and verified using python programming.
