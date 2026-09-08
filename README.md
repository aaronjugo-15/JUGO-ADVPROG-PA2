# ECE 2112: Advanced Computer Programming and Algorithms
## EXPERIMENT 2: NUMERICAL PYTHON (NUMPY)
### Aaron Siegfreid R. Jugo
### 2ECE-A
### 9/8/2026 

--------------------------------
Before doing the task, I imported Numpy in the notebook by using the code `import numpy as np`
### Task 1: REPRODUCIBLE NORMALIZATION PROBLEM

The first task is to create a reproducible random 5 × 5 integer ndarray named `X` by using the code:\


`np.random.seed(2112)`\
`X = np.random.randint(10, 101, size=(5, 5))`

And normalized the array by using the formula 

### **Z = (X - x̄)/σ**

where x̄ is the mean of all 25 elements, and σ is their population standard deviation as returned by
NumPy’s default std() call. 

The required checks are:
- Display X
- Display X_normalized
- Display mean
- Display standard deviation.
- normalized mean must be 0
- normalized standard deviation must be 1.

The correct solution has 15 selected elements; the first is 484, and the last is 1296.

Save the selected array as `X_normalized.npy`

To solve this, find the mean using the `.mean()` operator 

`mean = X.mean()`

and using the variable `std` to find the standard deviation of X

`std = X.std()`

Then, normalized the array by using the code

`X_normalized = (X - mean)/std`

This creates a new array `X_normalized` that normalizes the input array.

Display the mean, standard deviation, normalized array, normalized mean (using the `.mean()`), and the normalized standard deviation (using the `.std()`) using the code `print("quote", variable/array)`. 

Since the instruction is to round the floating-point value, the `round(X_normalized.mean(), 1)` is used to round up the value.

`np.random.seed(2112)`\
`X = np.random.randint(10, 101, size=(5, 5))`

`mean = X.mean()`\
`std = X.std()`

`X_normalized = (X - mean)/std`

`print("Array of X: \n", X)`\
`print("\n Normalized Array: \n", X_normalized)`\
`print("\n Mean: \n", mean)`\
`print("\nStandard Deviation: \n", std)`

`print("\n Normalized Mean: \n", round(X_normalized.mean(),1))`\
`print("\n Normalized Standard Deviation: \n", round(X_normalized.std(),1))`

After executing, the variable `X_normalized` is saved in a file using the code `np.save("X_normalized.npy", X_normalized)`

------------------------------------------------
### Task 2: CUBES DIVISIBLE BY 4 PROBLEM

The second task is to create the first 100 positive integers, cube every element, and reshape the result into a 10 × 10 ndarray named C. Thus, C begins with 13 and ends with 1003. Use a Boolean condition on C to obtain every cubed value divisible by 4. Store the selected values in div_by_4. 

The required checks are:
- Display the shape of C
- Display the array div_by_4
- Display the number of selected elements.
  
A correct solution has 50 selected elements; the first is 8, and the last is 1,000,000.

Saved the selected array as `div_by_4.npy`

First, create variable 

























The required checks are:
1. Display S;
2. S mean;
3. above mean; and
4. The number of selected elements.










