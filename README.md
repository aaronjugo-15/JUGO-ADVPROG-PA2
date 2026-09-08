# ECE 2112: Advanced Computer Programming and Algorithms
## EXPERIMENT 2: NUMERICAL PYTHON (NUMPY)
### Aaron Siegfreid R. Jugo
### 2ECE-A
### 9/8/2026 


Before doing the task, I imported Numpy in the notebook by using the code `import numpy as np`
### Task 1: REPRODUCIBLE NORMALIZATION PROBLEM

We were tasked to first create a reproducible random 5 × 5 integer ndarray named `X` by using the code:\


`np.random.seed(2112)`\
`X = np.random.randint(10, 101, size=(5, 5))`

And normalized the array by using the formula 

### **Z = (X - x̄)/σ**

where  x̄ is the mean of all 25 elements, and σ is their population standard deviation as returned by
NumPy’s default std() call. 

To solve this, I first find the mean by the `.mean()` operator 

`mean = X.mean()`

and using the variable `std` to find the standard deviation of X

`std = X.std()`

I then normalized the array by using the code

`X_normalized = (X - mean)/std`

With this, it creates a new array `X_normalized` that 





