# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Start and Input the Data

2.Compute the Mean of X and Y

3.Calculate the Slope (m) and Intercept (b)

4.Predict Y Values Using the Regression Equation

5.Display Results and Plot the Best Fit Line
## Program:
```

Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: Mugilarasi E
RegisterNumber: 25017644

import numpy as np
import matplotlib.pyplot as plt

# Input arrays safely using input strings
x = np.array(list(map(float, input("Enter x values separated by commas: ").split(','))))
y = np.array(list(map(float, input("Enter y values separated by commas: ").split(','))))

# Calculating means
x_mean = np.mean(x)
y_mean = np.mean(y)

# Calculating slope (m) and intercept (b) using the formula
num = np.sum((x - x_mean) * (y - y_mean))
denom = np.sum((x - x_mean) ** 2)
m = num / denom
b = y_mean - m * x_mean

print("Slope (m):", m)
print("Intercept (b):", b)

# Predict y values
y_predicted = m * x + b
print("Predicted y values:", y_predicted)

# Plotting
plt.scatter(x, y, label="Original Data")
plt.plot(x, y_predicted, color='red', label="Best Fit Line")
plt.xlabel("x")
plt.ylabel("y")
plt.title("Linear Regression")
plt.legend()
plt.grid(True)
plt.show()

```

## Output:
<img width="768" height="674" alt="Screenshot 2025-10-04 114127" src="https://github.com/user-attachments/assets/b411e107-202f-4505-8d6f-d63d9097185f" />




## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
