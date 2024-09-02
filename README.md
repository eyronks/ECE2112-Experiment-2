# ECE2112 Programming Problems

This repository contains Python scripts for solving various programming problems in ECE2112. The problems are focused on creating arrays and using the NumPy library for numerical analysis. Below are the details of each script included in this repository:

## Scripts

### Normalization Problem

**Instructions:** In this problem, create a random 5 x 5 ndarray and store it to variable X. Normalize X. Save your normalized ndarray as X_normalized.npy

**Function:**
```python
# Import numerical python library
import numpy as np

# Create a random 5x5 ndarray
np.random.seed(0)  # To ensure that the same random array is generated
X = np.random.rand(5, 5)

# Calculate the mean and standard deviation of the array
mean = X.mean()
std = X.std()

# Normalize the array
X_normalized = (X - mean) / std

# Print the original and normalized arrays
print("Original Array:")
print(X)
print("\nNormalized Array:")
print(X_normalized)

# Save the normalized array as X_normalized.npy
np.save('X_normalized.npy', X_normalized)
```

**Output:**

Original Array:

[[0.5488135  0.71518937 0.60276338 0.54488318 0.4236548 ]
 [0.64589411 0.43758721 0.891773   0.96366276 0.38344152]
 [0.79172504 0.52889492 0.56804456 0.92559664 0.07103606]
 [0.0871293  0.0202184  0.83261985 0.77815675 0.87001215]
 [0.97861834 0.79915856 0.46147936 0.78052918 0.11827443]]

Normalized Array:

[[-0.14854421  0.44055117  0.04247881 -0.1624605  -0.59169993]
 [ 0.19519398 -0.54236874  1.06578972  1.32033341 -0.73408512]
 [ 0.71154487 -0.21907095 -0.08045184  1.18555078 -1.84023484]
 [-1.78325269 -2.02016749  0.85634317  0.66350295  0.98873998]
 [ 1.37328739  0.73786513 -0.4577726   0.67190312 -1.67297558]]

 ### Divisible by 3 Problem

**Instructions:** In this problem, create a 10 x 10 ndarray which are the squares of the first 100 positive integers. From this ndarray, determine all the elements that are divisible by 3. Save the result as div_by_3.np.yy.

**Function:**
```python
# Import numerical python library
import numpy as np

# Create the 10x10 array of squares
A = np.array([i**2 for i in range(1, 101)]).reshape(10, 10)

# Find the elements divisible by 3
div_by_3 = A[A % 3 == 0]

# Save the result
np.save('div_by_3.npy', div_by_3)
```
