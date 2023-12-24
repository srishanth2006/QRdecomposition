# Algorithm for QR Decomposition
## Aim:
To implement QR decomposition algorithm using the Gram-Schmidt method.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Intialize the matrix Q and u
2.	The vector u and e is given by

    ![eqn1](./ex4.jpg)

    ![eqn2](./ex6.jpg)

    ![eqn3](./ex3.jpg)

3.	Obtain the Q matrix   
    ![eqn4](./ex1.jpg)
4.	Construct the upper triangular matrix R
    ![eqn5](./ex2.jpg)



## Program:
### Gram-Schmidt Method
```''' 
Program to QR decomposition using the Gram-Schmidt method
Developed by: your name SRISHANTH J
RegisterNumber: 212223240160
'''
import numpy as np
def QR_Decomposition(A):
    n,m=a.shape
    Q=np.empty((n,n))
    u=np.empty((n,n))
    u[:,0]=A[:,0]
    Q[:,0]=u[:,0]/np.linalg.norm(u[:,0])
    for i in range(1,n):
         u[:,i]=A[:,i]
         for j in range(i):
             u[:,i]-=(A[:,i]@Q[:,j])*Q[:,j]
         Q[:,i]=u[:,i]/np.linalg.norm(u[:,i])
    R=np.zeros((n,m))
    for i in range(n):
        for j in range(i,m):
            R[i,j]=A[:,j]@Q[:,i]
    print(Q)
    print(R)
a=np.array(eval(input())) 
QR_Decomposition(a)
             
        
 







```

## Output
```
<img width="671" alt="Screenshot 2023-12-24 200135" src="https://github.com/srishanth2006/QRdecomposition/assets/150319470/eae17b7c-c107-4fc7-8303-82cbe96842a1">

```
## Result
Thus the QR decomposition algorithm using the Gram-Schmidt process is written and verified the result.
