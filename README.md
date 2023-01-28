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
``` python
 
'''
 Program for Univariat linear regression
 using the least squere method
 Developed By : kamalesh.E
 Register Number:22004792
'''
import numpy as np
# Preprocessing Input data
X = np.array(eval(input()))
Y = np.array(eval(input()))

# Building the model 
X_mean=np.mean(X)
Y_mean=np.mean(Y)

num=0
denom=0

for i in range(len(X)):
    num+=(X[i]-X_mean)*(Y[i]-Y_mean)
    denom+=(X[i]-X_mean)**2

m=num/denom
c=Y_mean-m*X_mean

print (m, c)

#Predict the output
Y_pred=m*X+c
print (Y_pred)

import matplotlib.pyplot as plt
plt.scatter(X,Y,color = 'blue')
plt.plot(X,Y_pred,color = 'red')
plt.title('xv=y')
plt.show()
```

## Output
##[](input.jpg.png)


## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
