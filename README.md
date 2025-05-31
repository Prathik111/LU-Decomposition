# LU Decomposition 

## AIM:
To write a program to find the LU Decomposition of a matrix.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
Step 1: Input the matrix A from the user.
Step 2: Perform LU decomposition on A to obtain P, L, U such that PA = LU.
Step 3: Extract the lower triangular matrix L and upper triangular matrix U.
Step 4: Print the matrices L and U.

(ii)
Step 1: Input the matrix A and the vector b from the user.
Step 2: Compute the LU factorization of A using lu_factor to get lu and piv.
Step 3: Solve the system AX = b by applying lu_solve with the LU factors and pivots.
Step 4: Print the solution vector X.  

## Program:
(i) To find the L and U matrix
```
'''Program to find L and U matrix using LU decomposition.
Developed by: Prathik TS
RegisterNumber: 212224240117
'''
import numpy as np
from scipy.linalg import lu,solve_triangular

a=np.array(eval(input()))
p,l,u=lu(a)
print(l)
print(u)
```
(ii) To find the LU Decomposition of a matrix
```
'''Program to solve a matrix using LU decomposition.
Developed by: Prathik TS
RegisterNumber: 212224240117
'''

# To print X matrix (solution to the equations)
import numpy as np
from scipy.linalg import lu,solve_triangular
a=np.array(eval(input()))
b=np.array(eval(input()))
p,l,u=lu(a)
pb=np.dot(p,b)
y=solve_triangular(l,pb,lower=True)
x=solve_triangular(u,y)
print(x) 
```

## Output:
![lu decomposition]()
![image](https://github.com/user-attachments/assets/4112a9ab-3dc9-408d-a8c6-6e19a22993a6)
![image](https://github.com/user-attachments/assets/d98eaa57-529a-452d-a839-bf043334421b)



## Result:
Thus the program to find the LU Decomposition of a matrix is written and verified using python programming.

