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
7.End the process

## Program:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: Tharun R
RegisterNumber: 212224230289
*/
import numpy as np
import matplotlib.pyplot as plt

# Sample data
x = np.array([1, 2, 3, 4, 5])
y = np.array([2, 4, 5, 4, 5])

# Step 1: Calculate means
x_mean = np.mean(x)
y_mean = np.mean(y)

# Step 2: Calculate slope (m) and intercept (c)
numerator = np.sum((x - x_mean) * (y - y_mean))
denominator = np.sum((x - x_mean)**2)
m = numerator / denominator
c = y_mean - m * x_mean

# Step 3: Predict values
y_pred = m * x + c

# Step 4: Plot the results
plt.scatter(x, y, color='blue', label='Actual')
plt.plot(x, y_pred, color='red', label='Best Fit Line')
plt.xlabel('x')
plt.ylabel('y')
plt.legend()
plt.title('Univariate Linear Regression')
plt.show()

# Optional: Print coefficients
print(f"Slope (m): {m}")
print(f"Intercept (c): {c}")
```

## Output:

<img width="807" height="646" alt="image" src="https://github.com/user-attachments/assets/c87808de-baf6-48bb-bec8-627ea5879d14" />


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
