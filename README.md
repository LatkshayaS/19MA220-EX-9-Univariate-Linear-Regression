
# EX-9-IMPLEMENTATION OF UNIVARIATE LINEAR RERESSION
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.
## EQUIPMENT REQUIRED:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## ALGORITHM:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 ![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```
# using coderunner

import numpy as np

# --- Preprocessing Input data ---
X = np.array(eval(input()))   # example input: [1,2,3,4,5]
Y = np.array(eval(input()))   # example input: [2,4,5,4,5]

# --- Building the model ---
X_mean = np.mean(X)
Y_mean = np.mean(Y)

num = 0
den = 0

for i in range(len(X)):
    num += (X[i] - X_mean) * (Y[i] - Y_mean)
    den += (X[i] - X_mean)**2

m = num / den
c = Y_mean - m * X_mean

print(m, c)

Y_pred = m * X + c
print(Y_pred)





```
## Output:
</br>![EX9.png]()
</br>
</br>
</br>

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
