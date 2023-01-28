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
 ![eq1](https://user-images.githubusercontent.com/118787261/214839783-0dd84fc6-db54-443d-8853-20a427f4cf8e.jpg)

4.	Compute the y -intercept of the line by using the formula:
 ![eq2](https://user-images.githubusercontent.com/118787261/214839805-f45a4933-e4dd-442d-9cfb-187ee9ac8419.jpg)

5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```python
''' 
Program for Univariate linear regression using the least squares method.
Developed by: kabilan T
RegisterNumber: 22009071
'''
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
    den+= (x[i]-xmean)**2
m = num/den
b = ymean - m*xmean
print(m,b)
ypred = m*x+b
print(ypred)

plt.scatter(x,y,color='Red')
plt.plot(x,ypred,color='Blue')
plt.show()

```

## Sample Input and Output
![input](https://user-images.githubusercontent.com/118787261/214839905-59db7139-5356-4572-88fb-4f400971149c.jpg)


## Output

![uni2](https://user-images.githubusercontent.com/118787261/214839937-b93ff567-2a67-43f4-89b5-6c9adc33a691.png)
![uni3](https://user-images.githubusercontent.com/118787261/214839955-a1dfb827-b19a-4d1e-8fa4-b5fa9703690d.png)



## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
