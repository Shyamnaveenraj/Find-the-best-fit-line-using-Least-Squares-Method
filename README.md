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
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: JAGAN A
RegisterNumber: 212221230037
*/
```

```
#IMPORT LIBRARIES
import numpy as np
import matplotlib.pyplot as plt

#GETTING VALUES OF X AND Y FROM USER
x=np.array(eval(input("Enter the values of x: ")))
y=np.array(eval(input("Enter the values of y: ")))

#FINDING THE MEAN OF X AND Y INPUTS
x_mean=np.mean(x)
print("x_mean=",x_mean)
y_mean=np.mean(y)
print("y_mean=",y_mean)

nume,deno=0,0
for i in range(len(x)):
    nume+=((x[i]-x_mean)*(y[i]-y_mean))
    deno+=(x[i]-x_mean)**2

#SLOPE
m=nume/deno
print("Slope m = ",m)

#INTERCEPT                   
b=y_mean-(m*(x_mean))         
print("b= ",b)

#LINE EQN
y_pred=m*x+b
print("Y pred= ",y_pred)

#When x=3
y_p3=m*3+b;
print("when x=3,y=",y_p3)

#GRAPH
print("Graph")
plt.scatter(x,y)
plt.plot(x,y_pred,color="red")
plt.show()
```

## Output:
<img width="578" alt="image" src="https://user-images.githubusercontent.com/93427376/225255660-370e8dd0-8c54-414b-8f8d-8d5fe5437159.png">

## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
