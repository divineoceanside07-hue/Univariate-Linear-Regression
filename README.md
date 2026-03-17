# Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 <img width="293" height="150" alt="image" src="https://github.com/user-attachments/assets/c53a6639-deb4-4d38-8944-a6e183e743ca" />

4.	Compute the y -intercept of the line by using the formula:
 <img width="200" height="57" alt="image" src="https://github.com/user-attachments/assets/ebb56978-3053-4e3a-a2df-5f034850a3da" />

5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```


import numpy as np
import matplotlib.pyplot as plt

# Sample data (you can change this)
x = np.array([1, 2, 3, 4, 5])
y = np.array([2, 4, 5, 4, 5])

# Number of observations
n = len(x)

# Calculate slope (m) and intercept (c) using least squares formula
m = (n*np.sum(x*y) - np.sum(x)*np.sum(y)) / (n*np.sum(x**2) - (np.sum(x))**2)
c = (np.sum(y) - m*np.sum(x)) / n

print("Slope (m):", m)
print("Intercept (c):", c)

# Predicted values
y_pred = m*x + c

# Plot the data points and regression line
plt.scatter(x, y, color='blue', label="Data Points")
plt.plot(x, y_pred, color='red', label="Regression Line")
plt.xlabel("X")
plt.ylabel("Y")
plt.title("Univariate Linear Regression using Least Squares")
plt.legend()
plt.show()





```
## Output
<img width="821" height="631" alt="image" src="https://github.com/user-attachments/assets/069aef7d-eda4-49b6-beca-0df194c95478" />

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
