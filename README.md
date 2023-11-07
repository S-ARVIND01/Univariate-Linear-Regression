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

   ![eqn1](./eq1.jpg)

5.	Compute the y -intercept of the line by using the formula:

   ![eqn2](./eq2.jpg)  
6.	Use the slope m and the y -intercept to form the equation of the line.
7.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```python
import numpy as np
import matplotlib.pyplot as plt
X=np.array(eval(input()))
Y=np.array(eval(input()))
Xmean = np.mean(X)
Ymean = np.mean(Y)
num,den = 0,0
for i in range(len(X)):
    num += (X[i]-Xmean)*(Y[i]-Ymean)
    den += (X[i]-Xmean)**2
m = num/den
c = Ymean - m*Xmean
print(m,c)
Y_pred = m*X + c
print(Y_pred)
plt.scatter(X,Y)
plt.plot(X,Y_pred, color = "red")
plt.show()
```
## Output
![Screenshot 2023-11-07 093705](https://github.com/S-ARVIND01/Univariate-Linear-Regression/assets/118707337/51920b42-1727-4b49-a97e-e1ec4feb33e5)

![Screenshot 2023-11-07 091957](https://github.com/S-ARVIND01/Univariate-Linear-Regression/assets/118707337/92a52824-d5f9-4a7e-82d0-0241e87d4b4c)
## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
