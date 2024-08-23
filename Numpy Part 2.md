# Numpy - Part 2
**Written by: Syed Muhammad Awais Raza**  
[LinkedIn](https://www.linkedin.com/in/syed-muhammad-awais-raza-905317278/) | [Email](mailto:awaisraza5424@gmail.com) | [GitHub](https://github.com/awai1s)

## NumPy: Essential Operations with Arrays

**Table of Contents**

1. [Concatenating 2D Arrays](#1-concatenating-2d-arrays)
2. [Creating a 3D Array](#2-creating-a-3d-array)
3. [Reshaping Arrays](#3-reshaping-arrays)
4. [Indexing and Slicing Arrays](#4-indexing-and-slicing-arrays)
5. [Using `hstack` and `vstack` Functions](#5-using-hstack-and-vstack-functions)
6. [Matrix or Matrices](#6-matrix-or-matrices)

## 1. Concatenating 2D Arrays

### Explanation
In NumPy, you can concatenate two 2D arrays using the `np.concatenate` function. The `axis` parameter specifies the axis along which the arrays will be joined:
- `axis=0`: Concatenate along rows (vertically).
- `axis=1`: Concatenate along columns (horizontally).

### Code Example
```python
import numpy as np

# Creating two 2D arrays
array1 = np.array([[1, 2], [3, 4]])
array2 = np.array([[5, 6], [7, 8]])

# Concatenate along rows (axis=0)
concat_axis0 = np.concatenate((array1, array2), axis=0)
print("Concatenated along rows (axis=0):")
print(concat_axis0)

# Concatenate along columns (axis=1)
concat_axis1 = np.concatenate((array1, array2), axis=1)
print("\nConcatenated along columns (axis=1):")
print(concat_axis1)
```

### Output
```
Concatenated along rows (axis=0):
[[1 2]
 [3 4]
 [5 6]
 [7 8]]

Concatenated along columns (axis=1):
[[1 2 5 6]
 [3 4 7 8]]
```

## 2. Creating a 3D Array

### Explanation
A 3D array is an array with three axes. In NumPy, you can create a 3D array using `np.array`.

### Code Example
```python
# Creating a 3D array
array_example = np.array([[[0, 1, 2, 3],
                           [4, 5, 6, 7]],

                          [[0, 1, 2, 3],
                           [4, 5, 6, 7]],

                          [[0, 1, 2, 3],
                           [4, 5, 6, 7]]])
array_example
```

### Output
```
array([[[0, 1, 2, 3],
        [4, 5, 6, 7]],

       [[0, 1, 2, 3],
        [4, 5, 6, 7]],

       [[0, 1, 2, 3],
        [4, 5, 6, 7]]])
```

## 3. Reshaping Arrays

### Explanation
You can change the shape of an array using the `reshape` method.

### Code Example
```python
# Reshaping a 1D array to a 2D array
a = np.arange(12)
reshaped_array = a.reshape(3, 4)
print("Reshaped array (3x4):")
print(reshaped_array)
```

### Output
```
Reshaped array (3x4):
[[ 0  1  2  3]
 [ 4  5  6  7]
 [ 8  9 10 11]]
```

## 4. Indexing and Slicing Arrays

### Explanation
Indexing and slicing allow you to access and modify elements of an array. Filters can be used to extract elements based on conditions.

### Code Examples
```python
# Creating an array
b = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10])

# Simple indexing
print("Element at index 2:", b[2])

# Slicing
print("Elements from index 1 to 5:", b[1:6])

# Using filters
filtered_array = b[(b > 2) & (b < 11) & (b % 2 == 0)]
print("Filtered array (elements > 2, < 11, and even):", filtered_array)

# Advanced slicing
print("Elements from index 0 to 9 with step 2:", b[0:10:2])
```

### Output
```
Element at index 2: 3
Elements from index 1 to 5: [2 3 4 5 6]
Filtered array (elements > 2, < 11, and even): [ 4  6  8 10]
Elements from index 0 to 9 with step 2: [1 3 5 7 9]
```

## 5. Using `hstack` and `vstack` Functions

### Explanation
`hstack` stacks arrays horizontally (column-wise) while `vstack` stacks arrays vertically (row-wise).

### Code Examples
```python
# Creating two 2D arrays
array1 = np.array([[1, 2], [3, 4]])
array2 = np.array([[5, 6], [7, 8]])

# Horizontal stack
hstacked_array = np.hstack((array1, array2))
print("Horizontally stacked array:")
print(hstacked_array)

# Vertical stack
vstacked_array = np.vstack((array1, array2))
print("\nVertically stacked array:")
print(vstacked_array)
```

### Output
```
Horizontally stacked array:
[[1 2 5 6]
 [3 4 7 8]]

Vertically stacked array:
[[1 2]
 [3 4]
 [5 6]
 [7 8]]
```

## 6. Matrix or Matrices

### Explanation
Matrices are 2D arrays that are used extensively in linear algebra. NumPy provides a matrix class `np.matrix` which is a specialized 2D array.

### Code Examples
```python
# Creating a matrix
matrix1 = np.matrix([[1, 2], [3, 4]])
print("Matrix 1:")
print(matrix1)

# Matrix multiplication
matrix2 = np.matrix([[5, 6], [7, 8]])
matrix_product = matrix1 * matrix2
print("\nMatrix multiplication (Matrix 1 * Matrix 2):")
print(matrix_product)

# Matrix transpose
matrix_transpose = matrix1.T
print("\nTranspose of Matrix 1:")
print(matrix_transpose)
```

### Output
```
Matrix 1:
[[1 2]
 [3 4]]

Matrix multiplication (Matrix 1 * Matrix 2):
[[19 22]
 [43 50]]

Transpose of Matrix 1:
[[1 3]
 [2 4]]
```
