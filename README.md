# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1..Get the matrix from user.

2.Using "from numpy as np" to import numpy.

3.Using numpy library we solve the matrix using gaussian elimination with partial pivoting.

4.Print the result matrices (Gaussian Elimination).

5.End the program. 
imination). 

## Program:
```
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: S.E.Elamaran
RegisterNumber: 22000420
import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)

for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
    
for i in range(n):
    if a[i][j]==0.0:
        sys.exit('divide by zero found!')
    
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        
        for k in range(n+1):
            a[j][k]=a[j][k]-ratio*a[i][k]
            
x[n-1]=a[n-1][n]/a[n-1][n-1]

for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
        
    x[i]=x[i]/a[i][i]
    
for i in range(n):
    print('X%d = %0.2f'%(i,x[i]),end = ' ')
    
```

## Output:
![gaussian elimination](14d.png)


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

