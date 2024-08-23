# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

Step 1: start

Step 2: Get the independent variable X and dependent variable Y.

Step 3: Calculate the mean of the X -values and the mean of the Y -values.

Step 4: Find the slope m of the line of best fit using the formula. 

<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">

Step 5: Compute the y -intercept of the line by using the formula:

<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">

Step 6: Use the slope m and the y -intercept to form the equation of the line.

Step 7: Obtain the straight line equation Y=mX+b and plot the scatterplot.

Step 8: end 

## Program:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: NARRA AKHIL
RegisterNumber: 212223230136
*/
import numpy as np
import matplotlib.pyplot as plt
# Preprocessing Input data
X = np.array(eval(input()))
Y = np.array(eval(input()))
#Mean
X_mean =np.mean(X)
Y_mean =np.mean(Y)
num=0 #for slope
denom=0#for slope
#to find sum of (xi-x') & (yi-y') & (xi-x')^2
for i in range(len(X)):
    num+=(X[i] -X_mean)*(Y[i]-Y_mean)
    denom+= (X[i]-X_mean)**2
#calculate slope    
m=num/denom
#calculate intercept
b=Y_mean-m*X_mean
print(m,b)
#line equation
y_predicted=m*X+b
print(y_predicted)
#to plot graph
plt.scatter(X,Y)
plt.plot(X,y_predicted,color='red')
plt.show()
```
## Output:
## slope and y_intercept
![Screenshot 2024-08-23 110719](https://github.com/user-attachments/assets/a49dc7de-da55-41b9-b4c7-6bb74a24056d)
## y predicted
![Screenshot 2024-08-23 113323](https://github.com/user-attachments/assets/e1d00236-ddfc-4b38-a8e1-30a4177ef765)
## Graph
![Screenshot 2024-08-23 113330](https://github.com/user-attachments/assets/753cf95b-28d9-4374-a87a-475ceb11d325)
## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
