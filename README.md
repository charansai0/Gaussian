# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. start the program
2. import numpy and sys module to use the built-in functions for calculation
3. use for loop for find the solution 
4. end the program

## Program:
~~~
#Program to find the solution of a matrix using Gaussian Elimination.

#Developed by: v.charan sai

#RegisterNumber: 21003158

import numpy as np

import sys

n = int(input())

a = np.zeros((n,n+1))

X = np.zeros(n)

for i in range(n):

    for j in range(n+1):

        a[i][j] = float(input())

for i in range(n):

    if a[i][i] == 0.0:

        sys.exit('Divide by zero detected')

    for j in range(i+1, n):

        ratio = a[j][i]/a[i][i]

        for k in range(n+1):

            a[j][k] = a[j][k] - ratio * a[i][k]

X[n-1] = a[n-1][n]/a[n-1][n-1]

for i in range(n-2,-1,-1):

    X[i] = a[i][n]

    for j in range(i+1,n):

        X[i] = X[i] - a[i][j]*X[j]

    X[i] = X[i]/a[i][i]

for i in range(n):

    print('X%d = %0.2f' %(i,X[i]), end = ' ')

~~~
## Output:
![gaussian elimination](https://github.com/charansai0/Gaussian/blob/main/Screenshot%20(161).png?raw=true)


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

