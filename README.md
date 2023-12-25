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
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```
#Program to implement univariate Linear Regression to fit a straight line using least squares.
#Developed by: Azeez Ahamad
#register number: 230003977

import numpy as np 
import matplotlib.pyplot as plt
x = np.array([0,1,2,3,4,5,6,7,8,9])
y = np.array([1,3,2,5,7,8,8,9,10,12])
plt.scatter(x,y)
plt.show()
xmean = np.mean(x)
ymean = np.mean(y)
num=0
den=0
for i in range(len(x)):
    num+=(x[i]-xmean)*(y[i]-ymean)
    den+=(x[i]-xmean)**2
m = num/den
b = ymean - m*xmean
print(m,b)
ypred = m*x+b
print(ypred)


plt.scatter(x,y,color='Red')
plt.plot(x,ypred,color='Blue')
plt.show()





```
## Output
![Screenshot 2023-12-25 165544](https://github.com/jayadev133/Univariate-Linear-Regression/assets/150319465/ea7425e7-fe13-46a2-aa19-b86be4ded3d4)
![Screenshot 2023-12-25 165627](https://github.com/jayadev133/Univariate-Linear-Regression/assets/150319465/6c17e8db-4ad2-493f-9dac-45d96013fc38)
![Screenshot 2023-12-25 165654](https://github.com/jayadev133/Univariate-Linear-Regression/assets/150319465/d93116cf-d073-4256-a601-ec0c29b1e2bf)


## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
