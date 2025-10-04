# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

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
