**Lecture 1: Introduction to NumPy**

- **Introduction:**
  - What is NumPy and why is it important?
  - Installation and importing NumPy.
  
- **Getting Started:**
  - Creating NumPy arrays.
  - Basic operations on arrays.
  - Array attributes and methods.

**Lecture 2: NumPy Array Operations**

- **Array Operations:**
  - Element-wise operations with arrays.
  - Mathematical functions with arrays.
  - Broadcasting in NumPy.
  
- **Indexing and Slicing:**
  - Accessing elements and subarrays.
  - Indexing and slicing 1D and 2D arrays.
  - Fancy indexing.

**Lecture 3: Array Shape and Reshaping**

- **Array Shape:**
  - Understanding dimensions, shape, and size.
  - Changing the shape of an array.
  - Transposing arrays.
  
- **Array Reshaping:**
  - Reshaping arrays using `.reshape()` method.
  - Flattening arrays with `.ravel()` and `.flatten()`.

**Lecture 4: Array Aggregation and Broadcasting**

- **Aggregation Functions:**
  - Sum, mean, median, and more.
  - Aggregations along specific axes.
  
- **Broadcasting:**
  - Understanding broadcasting rules.
  - Applying arithmetic operations on arrays of different shapes.

**Lecture 5: Array Manipulation and Sorting**

- **Array Manipulation:**
  - Joining arrays using `np.concatenate()` and `np.vstack()`.
  - Splitting arrays using `np.split()` and `np.hsplit()`.
  
- **Array Sorting:**
  - Sorting arrays using `np.sort()` and `np.argsort()`.
  - Finding unique elements with `np.unique()`.

**Lecture 6: Array Filtering and Boolean Indexing**

- **Boolean Indexing:**
  - Creating boolean masks for indexing.
  - Applying boolean indexing to filter arrays.
  
- **Advanced Indexing:**
  - Combining fancy and boolean indexing.
  - Using `np.ix_` to create an open mesh.

**Lecture 7: Working with Dates and Times in NumPy**

- **Datetime Objects:**
  - Creating datetime arrays using `np.datetime64()`.
  - Performing arithmetic operations with datetime arrays.
  
- **Time Series Analysis:**
  - Creating a time series array.
  - Resampling and moving window functions.

**Lecture 8: Introduction to Linear Algebra with NumPy**

- **Vector and Matrix Operations:**
  - Vector addition, dot product, and cross product.
  - Matrix multiplication and inversion.
  
- **Eigenvalues and Eigenvectors:**
  - Calculating eigenvalues and eigenvectors.
  - Applications in data transformation and analysis.

**Lecture 9: Introduction to Random Sampling with NumPy**

- **Random Number Generation:**
  - Generating random numbers using `np.random`.
  - Generating random arrays of different distributions.
  
- **Random Sampling:**
  - Randomly sampling elements from an array.
  - Permutations and shuffling.

**Lecture 10: Introduction to File Input and Output with NumPy**

- **Saving and Loading Arrays:**
  - Saving arrays to disk using `np.save()` and `np.savez()`.
  - Loading saved arrays using `np.load()`.
  
- **Text File I/O:**
  - Reading and writing text files using `np.loadtxt()` and `np.savetxt()`.

# **Lecture 1: Introduction to NumPy**

**Introduction:**
NumPy, which stands for Numerical Python, is a fundamental package in Python for scientific computing. It provides support for arrays, which are multi-dimensional, homogenous data structures, and a wide range of mathematical functions to operate on these arrays. NumPy forms the foundation for many other scientific and data analysis libraries in Python.

**Why NumPy is Important:**
NumPy offers a range of benefits that make it a vital tool for data analysis and scientific computing:
- Efficiently handles large datasets and numerical computations.
- Provides multidimensional array objects that are more efficient and convenient than Python's built-in lists.
- Supports a wide variety of mathematical operations on arrays.
- Offers tools for integrating C/C++ and Fortran code.
- Forms the basis for other libraries like SciPy, pandas, scikit-learn, and more.

**Installation and Importing:**
Before using NumPy, you need to install it. You can use the following command in your terminal or command prompt:
```
pip install numpy
```

Once installed, you can import NumPy into your Python scripts or notebooks using the following line:



```python
import numpy as np
```

**Getting Started:**

**Creating NumPy Arrays:**
Arrays are the fundamental building blocks in NumPy. You can create arrays using various methods, such as from Python lists or using built-in functions.



```python
import numpy as np

# Creating a 1D array
arr1 = np.array([1, 2, 3, 4, 5])

# Creating a 2D array (matrix)
arr2 = np.array([[1, 2, 3], [4, 5, 6]])

print(arr1)
print()
print(arr2)
```

    [1 2 3 4 5]
    
    [[1 2 3]
     [4 5 6]]
    

**Basic Operations on Arrays:**
NumPy allows you to perform element-wise operations on arrays. These operations are much faster than using regular Python loops.



```python
# Basic operations
result = arr1 + 2       # Add 2 to each element
result = arr1 * 3       # Multiply each element by 3
result = arr1 ** 2      # Square each element
```

**Array Attributes and Methods:**
Arrays have attributes that provide information about the array, such as its shape, dimensions, and size. They also come with methods for common mathematical operations.



```python
print(arr1.shape)       # Shape of the array (tuple)
print(arr2.ndim)        # Number of dimensions
print(arr2.size)        # Number of elements
print(arr2.sum())       # Sum of all elements
```

    (5,)
    2
    6
    21
    


```python
import numpy as np

arr1 = np.arange(10, 51)
print(arr1)

```

    [10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33
     34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50]
    


```python
import numpy as np

arr1 = np.arange(10, 51)
print("Array 1 -> ",arr1)
print()
result_of_sum = arr1 + 5
print("Result Of Sum Of Each Num by 5 -> ",result_of_sum)
print()
result_of_multiply = arr1 * 2
print("Result Of Multiply Of Each Num by 2 -> ",result_of_multiply)
```

    Array 1 ->  [10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33
     34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50]
    
    Result Of Sum Of Each Num by 5 ->  [15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38
     39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55]
    
    Result Of Multiply Of Each Num by 2 ->  [ 20  22  24  26  28  30  32  34  36  38  40  42  44  46  48  50  52  54
      56  58  60  62  64  66  68  70  72  74  76  78  80  82  84  86  88  90
      92  94  96  98 100]
    


```python
import numpy as np

arr2 = np.random.randint(1, 101, (3, 4))
print(arr2)

```

    [[10 52  6 42]
     [76 65 21 13]
     [18 87 83 63]]
    


```python
import numpy as np

even_array = np.arange(2, 21, 2)
print(even_array)

```

    [ 2  4  6  8 10 12 14 16 18 20]
    

## **Lecture 2: NumPy Array Operations**

- **Array Operations:**
  - **Element-wise operations with arrays.** NumPy arrays support element-wise operations, meaning operations are applied to corresponding elements of two or more arrays. This is particularly useful for mathematical operations, as you can perform operations on entire arrays without writing explicit loops.


```python
import numpy as np

arr1 = np.array([1, 2, 3])
arr2 = np.array([4, 5, 6])

addition = arr1 + arr2
subtraction = arr1 - arr2
multiplication = arr1 * arr2
division = arr1 / arr2

print("Addition:", addition)
print("Subtraction:", subtraction)
print("Multiplication:", multiplication)
print("Division:", division)

```

    Addition: [5 7 9]
    Subtraction: [-3 -3 -3]
    Multiplication: [ 4 10 18]
    Division: [0.25 0.4  0.5 ]
    

- **Array Operations:**
  - **Mathematical functions with arrays.**
      NumPy provides a wide range of mathematical functions that can be applied to arrays. These functions operate element-wise, producing new arrays with the results.


```python
import numpy as np

arr = np.array([0, 30, 45, 60, 90])

sine_values = np.sin(np.radians(arr))
cosine_values = np.cos(np.radians(arr))
square_root = np.sqrt(arr)
exponential = np.exp(arr)

print("Sine Values:", sine_values)
print("Cosine Values:", cosine_values)
print("Square Root:", square_root)
print("Exponential:", exponential)

```

    Sine Values: [0.         0.5        0.70710678 0.8660254  1.        ]
    Cosine Values: [1.00000000e+00 8.66025404e-01 7.07106781e-01 5.00000000e-01
     6.12323400e-17]
    Square Root: [0.         5.47722558 6.70820393 7.74596669 9.48683298]
    Exponential: [1.00000000e+00 1.06864746e+13 3.49342711e+19 1.14200739e+26
     1.22040329e+39]
    

- **Array Operations:**
  - **Broadcasting in NumPy.** Broadcasting is a powerful feature in NumPy that allows you to perform operations on arrays of different shapes and sizes. NumPy automatically broadcasts smaller arrays to match the shape of larger arrays, enabling element-wise operations.


```python
import numpy as np

arr = np.array([1, 2, 3, 4, 5])
scalar = 10

result = arr + scalar
print("Result:", result)

```

    Result: [11 12 13 14 15]
    

- **Indexing and Slicing:**
  - **Accessing elements and subarrays.** You can access individual elements of an array using indexing. Indexing in NumPy starts from 0. Slicing allows you to create subarrays from an array by specifying start, stop, and step values.


```python
import numpy as np

arr = np.array([10, 20, 30, 40, 50])

element = arr[2]    # Access element at index 2
slice = arr[1:4]     # Slice from index 1 to 3 (inclusive)
every_other = arr[::2]  # Get every other element

print("Element:", element)
print("Slice:", slice)
print("Every Other Element:", every_other)

```

    Element: 30
    Slice: [20 30 40]
    Every Other Element: [10 30 50]
    

- **Indexing and Slicing:**
  - **Indexing and slicing 1D and 2D arrays.** Similar indexing and slicing concepts apply to 2D arrays. You can access elements in a 2D array using row and column indices.


```python
import numpy as np

arr = np.array(
    [
    [1, 2, 3], 
    [4, 5, 6], 
    [7, 8, 9]
    ]
)

element = arr[1, 2]     # Access element at row 1, column 2
row_slice = arr[0, :]   # Get all elements of row 0
col_slice = arr[:, 1]   # Get all elements of column 1

print("Element:", element)
print("Row Slice:", row_slice)
print("Column Slice:", col_slice)

```

    Element: 6
    Row Slice: [1 2 3]
    Column Slice: [2 5 8]
    

- **Indexing and Slicing:**
  - **Fancy indexing.** Fancy indexing involves using an array of indices to select specific elements from an array. This can be particularly useful when you want to select non-contiguous elements.


```python
import numpy as np

arr = np.array([10, 20, 30, 40, 50])

indices = np.array([1, 3])  # Indices of elements to select
selected_elements = arr[indices]

print("Selected Elements:", selected_elements)

```

    Selected Elements: [20 40]
    

## **Lecture 3: Array Shape and Reshaping**

**Array Shape:**

**Understanding Dimensions, Shape, and Size:**
In NumPy, an array's shape describes its dimensions. For a 1D array, the shape is the number of elements. For a 2D array, it's a tuple representing rows and columns. The size is the total number of elements.


```python
import numpy as np

arr = np.array([1,2])

shape = arr.shape       # Shape of the array (rows, columns)
dimensions = arr.ndim   # Number of dimensions
size = arr.size         # Total number of elements

print("Shape:", shape)
print("Dimensions:", dimensions)
print("Size:", size)
```

    Shape: (2,)
    Dimensions: 1
    Size: 2
    


```python
import numpy as np

arr = np.array(
    [
        [1, 2, 3],
        [4, 5, 6],
        [7, 8, 9]
    ]
)

shape = arr.shape       # Shape of the array (rows, columns)
dimensions = arr.ndim   # Number of dimensions
size = arr.size         # Total number of elements

print("Shape:", shape)
print("Dimensions:", dimensions)
print("Size:", size)
```

    Shape: (3, 3)
    Dimensions: 2
    Size: 9
    


```python

import numpy as np

arr = np.array(
    [
        [
            [1, 2, 3],
            [4, 5, 6],
            [7, 8, 9]
        ]
    ]
)

shape = arr.shape       # Shape of the array (rows, columns)
dimensions = arr.ndim   # Number of dimensions
size = arr.size         # Total number of elements

print("Shape:", shape)
print("Dimensions:", dimensions)
print("Size:", size)
```

    Shape: (1, 3, 3)
    Dimensions: 3
    Size: 9
    


```python

import numpy as np

arr = np.array(
    [
        [
            [
                [1, 2, 3],
                [4, 5, 6],
                [7, 8, 9]
            ]
        ]
    ]
)

shape = arr.shape       # Shape of the array (rows, columns)
dimensions = arr.ndim   # Number of dimensions
size = arr.size         # Total number of elements

print("Shape:", shape)
print("Dimensions:", dimensions)
print("Size:", size)
```

    Shape: (1, 1, 3, 3)
    Dimensions: 4
    Size: 9
    

**Changing the Shape of an Array:**

You can change an array's shape using `.reshape()`. The new shape must have the same total number of elements.


**Array Reshaping:**

**Reshaping Arrays using `.reshape()` Method:**
You can reshape arrays using the `.reshape()` method. Ensure that the new shape is compatible with the original size.


```python
import numpy as np

arr = np.array([1, 2, 3, 4, 5, 6])

reshaped = arr.reshape(2, 3)  # Reshape to a 2x3 array
print("Reshaped Array:\n", reshaped)
```

    Reshaped Array:
     [[1 2 3]
     [4 5 6]]
    


```python
import numpy as np

arr = np.array([1, 2, 3, 4, 5, 6])

reshaped = arr.reshape(2, 3)  # Reshape to a 2x3 array
print("Reshaped Array:\n", reshaped)
```

    Reshaped Array:
     [[1 2 3]
     [4 5 6]]
    


```python
import numpy as np

arr = np.array([1, 2, 3, 4, 5, 6, 7, 8])

reshaped = arr.reshape(2, 4)  # Reshape to a 2x3 array
print("Reshaped Array:\n", reshaped)
```

    Reshaped Array:
     [[1 2 3 4]
     [5 6 7 8]]
    


```python
import numpy as np

arr = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9])

reshaped = arr.reshape(3, 3)  # Reshape to a 2x3 array
print("Reshaped Array:\n", reshaped)
```

    Reshaped Array:
     [[1 2 3]
     [4 5 6]
     [7 8 9]]
    

**Transposing Arrays:**

Transposing a 2D array swaps its rows and columns. It can be done using `.T`.


```python
import numpy as np

arr = np.array([[1, 2, 3], [4, 5, 6]])

transposed = arr.T
print("Original Array:\n", arr)
print("Transposed Array:\n", transposed)
```

    Original Array:
     [[1 2 3]
     [4 5 6]]
    Transposed Array:
     [[1 4]
     [2 5]
     [3 6]]
    


```python
import numpy as np

arr = np.array([[1, 2, 3, 4], [4, 5, 6, 7]])

transposed = arr.T
print("Original Array:\n", arr)
print("Transposed Array:\n", transposed)
```

    Original Array:
     [[1 2 3 4]
     [4 5 6 7]]
    Transposed Array:
     [[1 4]
     [2 5]
     [3 6]
     [4 7]]
    

**Flattening Arrays with `.ravel()` and `.flatten()`:**

Flattening an array means converting it to a 1D array. You can use `.ravel()` or `.flatten()`.



```python
import numpy as np

arr = np.array([[1, 2, 3], [4, 5, 6]])

flattened_ravel = arr.ravel()
flattened_flatten = arr.flatten()

print("Flattened using ravel:\n", flattened_ravel)
print("Flattened using flatten:\n", flattened_flatten)
```

    Flattened using ravel:
     [1 2 3 4 5 6]
    Flattened using flatten:
     [1 2 3 4 5 6]
    


```python
import numpy as np

arr = np.array([[1, 2, 3], [4, 5, 6]])
check = arr.ndim

flattened_ravel = arr.ravel()
flattened_flatten = arr.flatten()

check1 = flattened_ravel.ndim
check2 = flattened_flatten.ndim

print("Array:\n",arr)
print("Dimension -> ",check)
print()
print("Flattened using ravel:\n", flattened_ravel)
print("Dimension of Flattened using ravel -> ",check1)
print()
print("Flattened using flatten:\n", flattened_flatten)
print("Dimension of Flattened using flatten -> ",check2)
```

    Array:
     [[1 2 3]
     [4 5 6]]
    Dimension ->  2
    
    Flattened using ravel:
     [1 2 3 4 5 6]
    Dimension of Flattened using ravel ->  1
    
    Flattened using flatten:
     [1 2 3 4 5 6]
    Dimension of Flattened using flatten ->  1
    

## **Lecture 4: Array Aggregation and Broadcasting**

**Aggregation Functions:**

**Sum, Mean, Median, and More:**
NumPy provides several aggregation functions for summarizing data. Common functions include `sum`, `mean`, `median`, `min`, `max`, `std`, and `var`.



```python
import numpy as np

arr = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])

total_sum = np.sum(arr)
mean_value = np.mean(arr)
median_value = np.median(arr)
min_value = np.min(arr)
max_value = np.max(arr)
std_deviation = np.std(arr)
variance = np.var(arr)

print("Sum:", total_sum)
print("Mean:", mean_value)
print("Median:", median_value)
print("Min:", min_value)
print("Max:", max_value)
print("Standard Deviation:", std_deviation)
print("Variance:", variance)
```

    Sum: 45
    Mean: 5.0
    Median: 5.0
    Min: 1
    Max: 9
    Standard Deviation: 2.581988897471611
    Variance: 6.666666666666667
    

**Aggregations Along Specific Axes:**
You can apply aggregation functions along specific axes of a multidimensional array. Specify the `axis` parameter to indicate the axis along which the aggregation should be performed.



```python
import numpy as np

arr = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])

sum_rows = np.sum(arr, axis=1)  # Sum along rows
mean_cols = np.mean(arr, axis=0)  # Mean along columns

print("Sum along Rows:", sum_rows)
print("Mean along Columns:", mean_cols)
```

    Sum along Rows: [ 6 15 24]
    Mean along Columns: [4. 5. 6.]
    

**Broadcasting:**

**Understanding Broadcasting Rules:**
Broadcasting allows arithmetic operations on arrays of different shapes, making them compatible by implicitly duplicating values to match shapes.


```python
import numpy as np

arr = np.array([1, 2, 3, 4, 5])
scalar = 10

result = arr + scalar
print("Result after Broadcasting:", result)

```

    Result after Broadcasting: [11 12 13 14 15]
    


```python
import numpy as np

arr1 = np.array([[1, 2, 3], [4, 5, 6]])
arr2 = np.array([10, 20, 30])

result = arr1 + arr2  # Broadcasting
print("Result:\n", result)
```

    Result:
     [[11 22 33]
     [14 25 36]]
    


```python
import numpy as np

arr1 = np.array([1, 2, 3])
arr2 = np.array([10, 20, 30])

result = arr1 + arr2  # Broadcasting
print("Result:\n", result)
```

    Result:
     [11 22 33]
    

**Applying Arithmetic Operations on Arrays of Different Shapes:**

Broadcasting can also be applied to arrays of different shapes and dimensions.


```python
import numpy as np

arr1 = np.array([[1, 2, 3], [4, 5, 6]])
arr2 = np.array([10, 20])

result = arr1 + arr2[:, np.newaxis]  # Broadcasting with newaxis
print("Result:\n", result)
```

    Result:
     [[11 12 13]
     [24 25 26]]
    


```python
import numpy as np

arr = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])

total_sum = np.sum(arr)
mean_value = np.mean(arr)
median_value = np.median(arr)
min_value = np.min(arr)
max_value = np.max(arr)
std_deviation = np.std(arr)
variance = np.var(arr)

print("Sum:", total_sum)
print("Mean:", mean_value)
print("Median:", median_value)
print("Min:", min_value)
print("Max:", max_value)
print("Standard Deviation:", std_deviation)
print("Variance:", variance)
```

    Sum: 45
    Mean: 5.0
    Median: 5.0
    Min: 1
    Max: 9
    Standard Deviation: 2.581988897471611
    Variance: 6.666666666666667
    


```python
# Create two arrays and find the union of elements using `np.union1d()`.
import numpy as np

arr1 = np.array([1, 2, 3, 4, 5])
arr2 = np.array([3, 4, 5, 6, 7])

union_elements = np.union1d(arr1, arr2)
print("Union Elements:", union_elements)
```

    Union Elements: [1 2 3 4 5 6 7]
    


```python
# Create a 2D array and find the indices where elements are divisible by 3.

import numpy as np

arr = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])

divisible_by_3_indices = np.where(arr % 3 == 0)
print("Indices where Elements are Divisible by 3:", divisible_by_3_indices)
```

    Indices where Elements are Divisible by 3: (array([0, 1, 2], dtype=int64), array([2, 2, 2], dtype=int64))
    

## **Lecture 5: Array Manipulation and Sorting**



**Array Manipulation:**
- **Joining Arrays using `np.concatenate()` and `np.vstack()`:** NumPy provides functions to combine arrays either by stacking them vertically or horizontally. `np.concatenate()` combines arrays along a specified axis, while `np.vstack()` stacks arrays vertically (along the first axis).




```python
import numpy as np

arr1 = np.array([1, 2, 3])
arr2 = np.array([4, 5, 6])

# Join arrays vertically (along rows)
result = np.concatenate((arr1, arr2), axis=0)

print("Joined Array (Vertically):\n", result)

```

    Joined Array (Vertically):
     [1 2 3 4 5 6]
    


```python
import numpy as np

# Create two arrays
arr1 = np.array([[1, 2, 3], [4, 5, 6]])
arr2 = np.array([[7, 8, 9], [10, 11, 12]])

# Vertically stack the two arrays using np.vstack()
stacked_array = np.vstack((arr1, arr2))

print("Array 1:\n", arr1)
print("Array 2:\n", arr2)
print("Stacked Array (Vertically):\n", stacked_array)

```

    Array 1:
     [[1 2 3]
     [4 5 6]]
    Array 2:
     [[ 7  8  9]
     [10 11 12]]
    Stacked Array (Vertically):
     [[ 1  2  3]
     [ 4  5  6]
     [ 7  8  9]
     [10 11 12]]
    

**Array Manipulation:**
- **Splitting Arrays using `np.split()` and `np.hsplit()`:** You can split arrays into smaller sub-arrays using `np.split()`. It allows you to specify the number of equally-sized sub-arrays along a given axis. `np.hsplit()` splits arrays horizontally (along columns).


```python
import numpy as np

arr = np.array([1, 2, 3, 4, 5, 6])

# Split the array into three equal parts
result = np.split(arr, 3)

print("Split Arrays:\n", result)

```

    Split Arrays:
     [array([1, 2]), array([3, 4]), array([5, 6])]
    


```python
import numpy as np

# Create a 2D array
arr = np.array([[1, 2, 3, 4],
                [5, 6, 7, 8],
                [9, 10, 11, 12]])

# Horizontally split the array into two parts using np.hsplit()
split_parts = np.hsplit(arr, 2)

print("Original Array:\n", arr)
print("Split Arrays (Horizontally):\n", split_parts)

```

    Original Array:
     [[ 1  2  3  4]
     [ 5  6  7  8]
     [ 9 10 11 12]]
    Split Arrays (Horizontally):
     [array([[ 1,  2],
           [ 5,  6],
           [ 9, 10]]), array([[ 3,  4],
           [ 7,  8],
           [11, 12]])]
    

**Array Sorting:**
- **Sorting Arrays using `np.sort()` and `np.argsort()`:** `np.sort()` arranges the elements of an array in ascending order. If you want to retrieve the sorted indices instead of the sorted values, you can use `np.argsort()`.



```python
import numpy as np

arr = np.array([3, 1, 2, 5, 4])

# Sort the array in ascending order
sorted_arr = np.sort(arr)

print("Sorted Array (Ascending Order):\n", sorted_arr)

```

    Sorted Array (Ascending Order):
     [1 2 3 4 5]
    

**Array Sorting:**
- **Finding Unique Elements with `np.unique()`:** `np.unique()` returns the unique elements from an array. It can be useful for identifying distinct values in data.



```python
import numpy as np

arr = np.array([1, 2, 2, 3, 4, 4, 5])

# Find unique elements
unique_elements = np.unique(arr)

print("Unique Elements:\n", unique_elements)

```

    Unique Elements:
     [1 2 3 4 5]
    


```python
import numpy as np

# Create an unsorted array
arr = np.array([3, 1, 2, 5, 4])

# Get the sorted indices using np.argsort()
sorted_indices = np.argsort(arr)

print("Original Array:\n", arr)
print("Indices for Sorted Array:\n", sorted_indices)

```

    Original Array:
     [3 1 2 5 4]
    Indices for Sorted Array:
     [1 2 0 4 3]
    

## **Lecture 6: Array Filtering and Boolean Indexing**



- **Boolean Indexing:**
  - Creating boolean masks for indexing.


```python
import numpy as np

# Create an example array
arr = np.array([1, 2, 3, 4, 5])

# Create a boolean mask for elements greater than 3
boolean_mask = arr > 3

print("Original Array:\n", arr)
print("Boolean Mask:\n", boolean_mask)

```

    Original Array:
     [1 2 3 4 5]
    Boolean Mask:
     [False False False  True  True]
    

- **Boolean Indexing:**
  - Applying boolean indexing to filter arrays.


```python
import numpy as np

# Create an example array
arr = np.array([1, 2, 3, 4, 5])

# Create a boolean mask for elements greater than 3
boolean_mask = arr > 3

# Use the boolean mask to filter the array
filtered_array = arr[boolean_mask]

print("Original Array:\n", arr)
print("Boolean Mask:\n", boolean_mask)
print("Filtered Array:\n", filtered_array)

```

    Original Array:
     [1 2 3 4 5]
    Boolean Mask:
     [False False False  True  True]
    Filtered Array:
     [4 5]
    

- **Advanced Indexing:**
  - Combining fancy and boolean indexing.


```python
import numpy as np

# Create an example array
arr = np.array([1, 2, 3, 4, 5])

# Create an integer array for fancy indexing
indices = np.array([0, 2, 4])

# Use fancy indexing to select specific elements
selected_elements = arr[indices]

# Create a boolean mask for elements greater than 3
boolean_mask = arr > 3

# Use boolean indexing to filter elements
filtered_elements = arr[boolean_mask]

print("Original Array:\n", arr)
print("Selected Elements (Fancy Indexing):\n", selected_elements)
print("Boolean Mask:\n", boolean_mask)
print("Filtered Elements (Boolean Indexing):\n", filtered_elements)

```

    Original Array:
     [1 2 3 4 5]
    Selected Elements (Fancy Indexing):
     [1 3 5]
    Boolean Mask:
     [False False False  True  True]
    Filtered Elements (Boolean Indexing):
     [4 5]
    

- **Advanced Indexing:**
  - Using `np.ix_` to create an open mesh.


```python
import numpy as np

# Create two example arrays
arr1 = np.array([1, 2, 3])
arr2 = np.array([4, 5, 6])

# Use np.ix_ to create an open mesh for indexing
mesh = np.ix_(arr1, arr2)

print("Array 1:\n", arr1)
print("Array 2:\n", arr2)
print("Open Mesh:\n", mesh)

```

    Array 1:
     [1 2 3]
    Array 2:
     [4 5 6]
    Open Mesh:
     (array([[1],
           [2],
           [3]]), array([[4, 5, 6]]))
    

## **Lecture 7: Working with Dates and Times in NumPy**

- **Datetime Objects:**
  - Creating datetime arrays using `np.datetime64()`.


```python
import numpy as np

# Create a datetime array
dates = np.array(['2023-08-01', '2023-08-02', '2023-08-03'], dtype='datetime64')

print("Datetime Array:\n", dates)

```

    Datetime Array:
     ['2023-08-01' '2023-08-02' '2023-08-03']
    

- **Datetime Objects:**
  - Performing arithmetic operations with datetime arrays.


```python
import numpy as np

# Create two datetime arrays
dates1 = np.array(['2023-08-01', '2023-08-02', '2023-08-03'], dtype='datetime64')
dates2 = np.array(['2023-08-02', '2023-08-03', '2023-08-04'], dtype='datetime64')

# Calculate the time difference between the two arrays
time_difference = dates2 - dates1

print("Datetime Array 1:\n", dates1)
print("Datetime Array 2:\n", dates2)
print("Time Difference:\n", time_difference)

```

    Datetime Array 1:
     ['2023-08-01' '2023-08-02' '2023-08-03']
    Datetime Array 2:
     ['2023-08-02' '2023-08-03' '2023-08-04']
    Time Difference:
     [1 1 1]
    

- **Time Series Analysis:**
  - Creating a time series array.



```python
import numpy as np

# Create a time series array
start_date = np.datetime64('2023-08-01')
end_date = np.datetime64('2023-08-10')
time_series = np.arange(start_date, end_date, np.timedelta64(1, 'D'))

print("Time Series Array:\n", time_series)

```

    Time Series Array:
     ['2023-08-01' '2023-08-02' '2023-08-03' '2023-08-04' '2023-08-05'
     '2023-08-06' '2023-08-07' '2023-08-08' '2023-08-09']
    

- **Time Series Analysis:**
  - Resampling and moving window functions.


```python
import numpy as np

# Create a time series array
dates = np.array(['2023-08-01', '2023-08-02', '2023-08-03', '2023-08-04', '2023-08-05'], dtype='datetime64')

# Generate random data
data = np.array([10, 15, 12, 18, 20])

# Convert datetime to numeric values (days since epoch)
numeric_dates = (dates - np.datetime64('1970-01-01')).astype('int') / (3600 * 24 * 1e9)

# Resample to weekly frequency
start_date = numeric_dates[0]
end_date = numeric_dates[-1]
weekly_dates = np.arange(start_date, end_date, 7)

# Use np.interp() to resample the data
resampled_data = np.interp(weekly_dates, numeric_dates, data)

# Convert the resampled numeric dates back to datetime
resampled_dates = np.datetime64('1970-01-01') + (resampled_data * np.timedelta64(1, 'D'))

print("Original Dates:\n", dates)
print("Original Data:\n", data)
print("Resampled Dates (Weekly):\n", resampled_dates)
print("Resampled Data:\n", resampled_data)

```

    Original Dates:
     ['2023-08-01' '2023-08-02' '2023-08-03' '2023-08-04' '2023-08-05']
    Original Data:
     [10 15 12 18 20]
    Resampled Dates (Weekly):
     ['1970-01-11']
    Resampled Data:
     [10.]
    

## **Lecture 8: Introduction to Linear Algebra with NumPy**


- **Vector and Matrix Operations:**
  - Vector addition, dot product, and cross product.



```python
import numpy as np

# Create two vectors
vector1 = np.array([1, 2, 3])
vector2 = np.array([4, 5, 6])

# Vector addition
result_addition = vector1 + vector2

# Dot product
result_dot_product = np.dot(vector1, vector2)

# Cross product
result_cross_product = np.cross(vector1, vector2)

print("Vector 1:\n", vector1)
print("Vector 2:\n", vector2)
print("Vector Addition:\n", result_addition)
print("Dot Product:\n", result_dot_product)
print("Cross Product:\n", result_cross_product)

```

    Vector 1:
     [1 2 3]
    Vector 2:
     [4 5 6]
    Vector Addition:
     [5 7 9]
    Dot Product:
     32
    Cross Product:
     [-3  6 -3]
    

 - **Vector and Matrix Operations:**
    - Matrix multiplication and inversion.
  


```python
import numpy as np

# Create two matrices
matrix1 = np.array([[1, 2], [3, 4]])
matrix2 = np.array([[5, 6], [7, 8]])

# Matrix multiplication
result_matrix_multiply = np.dot(matrix1, matrix2)

# Matrix inversion
result_matrix_inverse = np.linalg.inv(matrix1)

print("Matrix 1:\n", matrix1)
print("Matrix 2:\n", matrix2)
print("Matrix Multiplication:\n", result_matrix_multiply)
print("Matrix Inversion:\n", result_matrix_inverse)

```

    Matrix 1:
     [[1 2]
     [3 4]]
    Matrix 2:
     [[5 6]
     [7 8]]
    Matrix Multiplication:
     [[19 22]
     [43 50]]
    Matrix Inversion:
     [[-2.   1. ]
     [ 1.5 -0.5]]
    

- **Eigenvalues and Eigenvectors:**
  - Calculating eigenvalues and eigenvectors.


```python
import numpy as np

# Create a matrix
matrix = np.array([[4, 2], [1, 3]])

# Calculate eigenvalues and eigenvectors
eigenvalues, eigenvectors = np.linalg.eig(matrix)

print("Matrix:\n", matrix)
print("Eigenvalues:\n", eigenvalues)
print("Eigenvectors:\n", eigenvectors)

```

    Matrix:
     [[4 2]
     [1 3]]
    Eigenvalues:
     [5. 2.]
    Eigenvectors:
     [[ 0.89442719 -0.70710678]
     [ 0.4472136   0.70710678]]
    

- **Eigenvalues and Eigenvectors:**
  - Applications in data transformation and analysis.



```python
import numpy as np

# Create a matrix (representing a data transformation)
matrix = np.array([[4, 2], [1, 3]])

# Calculate eigenvalues and eigenvectors
eigenvalues, eigenvectors = np.linalg.eig(matrix)

# Eigenvalues represent the scaling factor for each eigenvector
print("Matrix (Data Transformation):\n", matrix)
print("Eigenvalues (Scaling Factors):\n", eigenvalues)

# Eigenvectors represent the direction of maximum variance in the data
print("Eigenvectors (Direction of Maximum Variance):\n", eigenvectors)

# Application: Principal Component Analysis (PCA)
# PCA is a common technique that utilizes eigenvalues and eigenvectors for dimensionality reduction and data analysis.
# It helps identify the most important features (principal components) in a dataset.

# In this example, let's consider a dataset (data_matrix) and perform PCA using the eigenvalues and eigenvectors.
data_matrix = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])

# Calculate the mean of the data
mean_vector = np.mean(data_matrix, axis=0)

# Center the data (subtract the mean)
centered_data = data_matrix - mean_vector

# Calculate the covariance matrix
cov_matrix = np.cov(centered_data, rowvar=False)

# Calculate eigenvalues and eigenvectors of the covariance matrix
eigenvalues_pca, eigenvectors_pca = np.linalg.eig(cov_matrix)

# Sort eigenvalues and eigenvectors in descending order
sorted_indices = np.argsort(eigenvalues_pca)[::-1]
eigenvalues_pca = eigenvalues_pca[sorted_indices]
eigenvectors_pca = eigenvectors_pca[:, sorted_indices]

print("Original Data Matrix:\n", data_matrix)
print("Covariance Matrix:\n", cov_matrix)
print("Eigenvalues (PCA):\n", eigenvalues_pca)
print("Eigenvectors (PCA):\n", eigenvectors_pca)

```

    Matrix (Data Transformation):
     [[4 2]
     [1 3]]
    Eigenvalues (Scaling Factors):
     [5. 2.]
    Eigenvectors (Direction of Maximum Variance):
     [[ 0.89442719 -0.70710678]
     [ 0.4472136   0.70710678]]
    Original Data Matrix:
     [[1 2 3]
     [4 5 6]
     [7 8 9]]
    Covariance Matrix:
     [[9. 9. 9.]
     [9. 9. 9.]
     [9. 9. 9.]]
    Eigenvalues (PCA):
     [27.  0.  0.]
    Eigenvectors (PCA):
     [[ 0.57735027  0.         -0.81649658]
     [ 0.57735027 -0.70710678  0.40824829]
     [ 0.57735027  0.70710678  0.40824829]]
    

## **Lecture 9: Introduction to Random Sampling with NumPy** 

- **Random Number Generation:**
  - Generating random numbers using `np.random`.


```python
import numpy as np

# Generate a random number between 0 and 1
random_number = np.random.rand()

# Generate an array of random numbers between 0 and 1
random_array = np.random.rand(5)

# Generate a random integer between a specified range
random_integer = np.random.randint(1, 10)

print("Random Number between 0 and 1:\n", random_number)
print("Random Array between 0 and 1:\n", random_array)
print("Random Integer between 1 and 10:\n", random_integer)

```

    Random Number between 0 and 1:
     0.5732937659198483
    Random Array between 0 and 1:
     [0.40889981 0.18416393 0.21463077 0.56773084 0.20580663]
    Random Integer between 1 and 10:
     1
    

- **Random Number Generation:**
  - Generating random arrays of different distributions.


```python
import numpy as np

# Generate a random array from a normal distribution
normal_distribution = np.random.normal(0, 1, 5)

# Generate a random array from a uniform distribution
uniform_distribution = np.random.uniform(1, 10, 5)

print("Random Array from Normal Distribution:\n", normal_distribution)
print("Random Array from Uniform Distribution:\n", uniform_distribution)

```

    Random Array from Normal Distribution:
     [-0.75724386 -1.48402001 -1.53065144  0.18910804 -1.7604315 ]
    Random Array from Uniform Distribution:
     [2.82270872 3.80306272 8.6303052  1.69778864 8.5605464 ]
    

- **Random Sampling:**
  - Randomly sampling elements from an array.



```python
import numpy as np

# Create an array
original_array = np.array([1, 2, 3, 4, 5])

# Randomly sample elements from the array
sampled_elements = np.random.choice(original_array, size=3, replace=False)

print("Original Array:\n", original_array)
print("Sampled Elements:\n", sampled_elements)

```

    Original Array:
     [1 2 3 4 5]
    Sampled Elements:
     [4 3 2]
    

- **Random Sampling:**
  - Permutations and shuffling.


```python
import numpy as np

# Create an array
original_array = np.array([1, 2, 3, 4, 5])

# Permute the elements to create a random order
permuted_array = np.random.permutation(original_array)

# Shuffle the elements in-place
shuffled_array = np.random.shuffle(original_array)

print("Original Array:\n", original_array)
print("Permuted Array (Random Order):\n", permuted_array)
print("Shuffled Array (In-Place Shuffle):\n", original_array)

```

    Original Array:
     [4 3 5 2 1]
    Permuted Array (Random Order):
     [1 4 5 2 3]
    Shuffled Array (In-Place Shuffle):
     [4 3 5 2 1]
    

## **Lecture 10: Introduction to File Input and Output with NumPy**

- **Saving and Loading Arrays:**
  - Saving arrays to disk using `np.save()` and `np.savez()`.
  - Loading saved arrays using `np.load()`.


```python
import numpy as np

# Create an example array
data_array = np.array([1, 2, 3, 4, 5])

# Save the array to a binary file
np.save('data_array.npy', data_array)

# Save multiple arrays to a compressed binary file
np.savez('multiple_arrays.npz', array1=data_array, array2=data_array)

# Load the saved array from the file
loaded_array = np.load('data_array.npy')

# Load the saved arrays from the compressed file
loaded_arrays = np.load('multiple_arrays.npz')

print("Original Array:\n", data_array)
print("Loaded Array from .npy File:\n", loaded_array)
print("Loaded Arrays from .npz File:\n", loaded_arrays['array1'], loaded_arrays['array2'])

```

    Original Array:
     [1 2 3 4 5]
    Loaded Array from .npy File:
     [1 2 3 4 5]
    Loaded Arrays from .npz File:
     [1 2 3 4 5] [1 2 3 4 5]
    

- **Text File I/O:**
  - Reading and writing text files using `np.loadtxt()` and `np.savetxt()`.


```python
import numpy as np

# Create an example array
data_array = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])

# Save the array to a text file (CSV format)
np.savetxt('data_array.csv', data_array, delimiter=',')

# Load the array from the text file
loaded_array = np.loadtxt('data_array.csv', delimiter=',')

print("Original Array:\n", data_array)
print("Loaded Array from .csv File:\n", loaded_array)

```

    Original Array:
     [[1 2 3]
     [4 5 6]
     [7 8 9]]
    Loaded Array from .csv File:
     [[1. 2. 3.]
     [4. 5. 6.]
     [7. 8. 9.]]
    
