# Numpy - Part 1
**Written by: Syed Muhammad Awais Raza**  
[LinkedIn](https://www.linkedin.com/in/syed-muhammad-awais-raza-905317278/) | [Email](mailto:awaisraza5424@gmail.com) | [GitHub](https://github.com/awai1s)
## Table of Contents
- [Numpy - Part 1](#numpy---part-1)
  - [Table of Contents](#table-of-contents)
  - [Introduction](#introduction)
  - [Why Use NumPy?](#why-use-numpy)
  - [Creating Arrays](#creating-arrays)
    - [1D Array](#1d-array)
    - [2D Array](#2d-array)
    - [3D Array](#3d-array)
    - [Converting Rows to Columns in a 2D Array](#converting-rows-to-columns-in-a-2d-array)
  - [Array Initialization](#array-initialization)
    - [Zeros Array](#zeros-array)
    - [Ones Array](#ones-array)
    - [Full Array](#full-array)
    - [Identity Matrix](#identity-matrix)
  - [Array Attributes](#array-attributes)
  - [Basic Operations](#basic-operations)
  - [Array Creation Functions](#array-creation-functions)
    - [arange](#arange)
    - [linspace](#linspace)
  - [Type Casting](#type-casting)
  - [Sorting Arrays](#sorting-arrays)
  - [Concatenating Arrays](#concatenating-arrays)

## Introduction
NumPy is a famous Python library used for performing mathematical operations. As the name indicates, NumPy stands for "Numerical Python". It is widely used in scientific computing, data analysis, and machine learning due to its efficiency and ease of use.

**Installing** 

To install the NumPy library, use pip:
```bash
pip install numpy
```

**Importing** **NumPy**

To import the NumPy library, use the following code:
```python
import numpy as np
```

## Why Use NumPy?
NumPy provides support for arrays and enables efficient numerical operations. It is more efficient than Python lists for numerical operations because:
- The data type is the same for all elements in the array.
- Arrays are stored in contiguous memory blocks.
- NumPy operations are implemented in C, allowing for vectorized operations.
- Pandas, another popular data analysis library, is built on top of NumPy.

## Creating Arrays
### 1D Array
A 1D array consists of a single sequence of elements:
```python
a = np.arange(6)
print(a)
print(a.shape)
```
**Output:**
```
[0 1 2 3 4 5]
(6,)
```

### 2D Array
A 2D array comprises rows and columns:
```python
a2 = a[np.newaxis, :]
print(a2)
print(a2.shape)
```
**Output:**
```
[[0 1 2 3 4 5]]
(1, 6)
```

### 3D Array
A 3D array includes an additional axis, often used in image processing:
```python
a3 = a2[np.newaxis, :]
print(a3)
print(a3.shape)
```
**Output:**
```
[[[0 1 2 3 4 5]]]
(1, 1, 6)
```

### Converting Rows to Columns in a 2D Array
```python
a2 = a[:, np.newaxis]
print(a2)
print(a2.shape)
```
**Output:**
```
[[0]
 [1]
 [2]
 [3]
 [4]
 [5]]
(6, 1)
```

## Array Initialization
### Zeros Array
Create a 2D array of zeros:
```python
zeros = np.zeros((2, 5))
print(zeros)
```
**Output:**
```
array([[0., 0., 0., 0., 0.],
       [0., 0., 0., 0., 0.]])
```

### Ones Array
Create a 2D array of ones:
```python
ones = np.ones((2, 5))
print(ones)
```
**Output:**
```
array([[1., 1., 1., 1., 1.],
       [1., 1., 1., 1., 1.]])
```

### Full Array
Create a 2D array filled with a specific value:
```python
full = np.full((2, 5), 7.5)
print(full)
```
**Output:**
```
array([[7.5, 7.5, 7.5, 7.5, 7.5],
       [7.5, 7.5, 7.5, 7.5, 7.5]])
```

### Identity Matrix
Create an identity matrix:
```python
identity = np.eye(5)
print(identity)
```
**Output:**
```
array([[1., 0., 0., 0., 0.],
       [0., 1., 0., 0., 0.],
       [0., 0., 1., 0., 0.],
       [0., 0., 0., 1., 0.],
       [0., 0., 0., 0., 1.]])
```

## Array Attributes
- **Data type of elements:** `a.dtype`
- **Type of array:** `type(a)`
- **Shape of array:** `a.shape`
- **Size of array:** `a.size`
- **Length of array:** `len(a)`
- **Dimension of array:** `a.ndim`

## Basic Operations
**Addition**
```python
h = a + b
print(h)
# Alternatively
x = np.add(a, b)
print(x)
```

**Subtraction**
```python
g = a - b
print(g)
```

**Division**
```python
e = a / b
print(e)
```

**Multiplication**
```python
k = a * b
print(k)
```

**Square** of Each Element
```python
q = a ** 2
print(q)
```

## Array Creation Functions
### arange
Create an array with a range of values:
```python
x = np.arange(23)
print(x)
```

Create an array of even numbers:
```python
even = np.arange(0, 23, 2)
print(even)
```
**Output:**
```
array([ 0,  2,  4,  6,  8, 10, 12, 14, 16, 18, 20, 22])
```

Create an array of odd numbers:
```python
odd = np.arange(1, 23, 2)
print(odd)
```
**Output:**
```
array([ 1,  3,  5,  7,  9, 11, 13, 15, 17, 19, 21])
```

### linspace
Generate a specific number of values between a range:
```python
lin = np.linspace(0, 10, num=15)
print(lin)
```
**Output:**
```
array([ 0.        ,  0.71428571,  1.42857143,  2.14285714,  2.85714286,
        3.57142857,  4.28571429,  5.        ,  5.71428571,  6.42857143,
        7.14285714,  7.85714286,  8.57142857,  9.28571429, 10.        ])
```

## Type Casting
Define the data type of an array:
```python
x = np.arange(0, 22.6, 1.5, dtype=np.int8)
print(x)
```
**Output:**
```
array([ 0,  1,  3,  4,  6,  7,  9, 10, 12, 13, 15, 16, 18, 19, 21], dtype=int8)
```

## Sorting Arrays
**Sorting in Ascending Order**
```python
arr = np.array([2, 1, 5, 3, 7, 4, 6, 8])
arr = np.sort(arr)
print(arr)
```
**Output:**
```
array([1, 2, 3, 4, 5, 6, 7, 8])
```

**Sorting in Descending Order**
```python
arr = np.sort(arr)[::-1]
names = np.array(['Alice', 'Bob', 'Charlie', 'David'])
names = np.sort(names)[::-1]
print(arr)
print(names)
```
**Output:**
```
array([8, 7, 6, 5, 4, 3, 2, 1])
array(['David', 'Charlie', 'Bob', 'Alice'], dtype='<U7')
```

## Concatenating Arrays
```python
a = np.array([1, 2, 3, 4, 5])
b = np.array([6, 7, 8, 9, 10])
c = np.concatenate((a, b))
print(c)
```
**Output:**
```
array([ 1,  2,  3,  4,  5,  6,  7,  8,  9, 10])
```

---

