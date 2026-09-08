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

With this, it creates a new array `X_normalized` that normalizes the array.

Using the `print("quote", variable/array)`, I printed the mean, standard deviation, normalized array, normalized mean (using the `.mean()`), and normalized standard deviation (using the `.std()`)

Since the instruction is to round the floating point and the value of normalized standard deviation must be 1, I used the `round(X_normalized.std, 1)` to round up the value.

`np.random.seed(2112)`\
`X = np.random.randint(10, 101, size=(5, 5))`

`mean = X.mean()`\
`std = X.std()`

`X_normalized = (X - mean)/std`

`print("Array of X: \n", X)`\
`print("\n Normalized Array: \n", X_normalized)`\
`print("\n Mean: \n", mean)`\
`print("\nStandard Deviation: \n", std)`

`print("\n Normalized Mean: \n", X_normalized.mean())`\
`print("\n Normalized Standard Deviation: \n", round(X_normalized.std(),1))`











