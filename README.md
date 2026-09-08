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

Display the mean, standard deviation, normalized array, normalized mean (using the `.mean()`), and the normalized standard deviation (using the `.std()`) using the code `print("name", variable/array)`. 

Since the instruction is to round the floating-point value, the `round(X_normalized.mean(), 1)` is used to round up the value.

`print("Array of X: \n", X)`\
`print("\n Normalized Array: \n", X_normalized)`\
`print("\n Mean: \n", mean)`\
`print("\nStandard Deviation: \n", std)`

`print("\n Normalized Mean: \n", X_normalized.mean())`\
`print("\n Normalized Standard Deviation: \n", round(X_normalized.std(),1))`

Thus, the full code is:

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

The output matched the intended result of 15 selected elements, with the first element 484, and the last element 1296.

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

First, create a variable named `d` that creates an array of the first 100 positive integers by using the `.arange(1,101,1)`.

`d = np.arange(1,101,1)`

Create another variable named `p` that cubes the variable `d` using `d**3`.

`p = d ** 3`

Assign variable `C` that reshapes the array `p` into 10 rows and 10 columns using `.reshape(10,10)`

`C = p.reshape(10,10)`

Use `div_by_4` to create a boolean function for the variable `C` that gets the element that is divisible by 4 using the code `C[C %4 == 0]`.

`div_by_4 = C[C % 4 ==0]`

Display the shape of C (using `.shape`), the array of div_by_4, and the number of selected elements (using `.save`) using the function `print("name", variable/array)`

`print("Shape of C:\n", C.shape)`\
`print("\n Arrays divisible by 4: \n", div_by_4) `\
`print("\n Number of Selected Elements:\n", div_by_4.size)`

Thus, the full code is:

`d = np.arange(1,101,1)`\
`p = d ** 3`

`C = p.reshape(10,10)`


`div_by_4 = C[C % 4 ==0]`

`print("Shape of C:\n", C.shape)`\
`print("\n Arrays divisible by 4: \n", div_by_4) `\
`print("\n Number of Selected Elements:\n", div_by_4.size)`

The output matched the intended result of 50 selected elements. The first element is 8, and the last element is 1,000,000.

After executing, the array `div_by_4` is saved in a file using the code `np.save("div_by_4.npy", div_by_4)`

----------------------------------------------------------------------------------------------------------

### Task 3: ABOVE-MEAN SQUARES PROBLEM

The last task is to create a 6 × 6 ndarray named S containing the squares of the first 36 positive integers in increasing row-major order. Compute the mean of all elements of S and store it in S mean. Then use Boolean filtering to select only the elements strictly greater than the S mean. 

The required checks are:
1. Display S
2. Display S mean
3. Display above mean
4. Display the number of selected elements

The correct solution has 15 selected elements; the first is 484, and the last is 1296.

First, create a variable `S` and make the first 36 positive integers using `np.arange(1,37,1)`, square them using `**2`, and reshape the entire statement using `.reshape(6,6)`.

`S = (np.arange(1,37,1) **2).reshape(6,6)`

Second, make the variable `S_mean` to find the mean of variable `S` using `.mean()`/

`S_mean = S.mean()`

Third, make the variable `above_mean` to get the elements that are greater than the `S_mean` using a boolean condition.

`above_mean = S[S>S_mean]`

Lastly, display S, S_mean, above_mean, and the number of selected elements using the function `print("name", variable/array)`

`print("Arrays of S:\n", S)`\
`print("\n Means of S: \n", S_mean)`\
`print("\n Above Mean squares:\n", above_mean.reshape(5,3))`\
`print("\n Number of Selected Elements:\n", above_mean.size)`

Thus, the full code is:

`S = (np.arange(1,37,1) **2).reshape(6,6)`\
`S_mean = S.mean()`\
`above_mean = S[S>S_mean]`

`print("Arrays of S:\n", S)`\
`print("\n Means of S: \n", S_mean)`\
`print("\n Above Mean squares:\n", above_mean.reshape(5,3))`\
`print("\n Number of Selected Elements:\n", above_mean.size)`

The output matched the intended result of 15 selected elements. The first element is 484, and the last element is 1296.

After executing, the array `above_mean` is saved in a file using the code `np.save("above_mean.npy", above_mean)`









