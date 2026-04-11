# Experiment 8: Tools or EDA - Study of NumPy Library

## 1. Aim
To study and understand the NumPy library in Python, focusing on its array structures, dimensionality, and built-in mathematical functions for efficient data manipulation.

## 2. Objectives
* To understand why NumPy is preferred over standard Python lists regarding speed and memory efficiency.
* To learn how to declare and manipulate 1D and 2D NumPy arrays.
* To study array attributes such as `ndim`, `shape`, and `dtype`.
* To explore built-in initialization functions such as `zeros()`, `ones()`, `eye()`, and `linspace()`.
* To perform basic statistical operations including Mean, Median, Sum, and Min/Max.

---

## 3. Theory

### A. Introduction to NumPy
**NumPy** (Numerical Python) is a fundamental library for scientific computing in Python. It provides support for large, multi-dimensional arrays and matrices, along with a collection of high-level mathematical functions to operate on these arrays.

### B. Why NumPy over Lists?
* **Performance:** NumPy arrays are stored in contiguous memory locations, making them significantly faster than Python lists for numerical processing.
* **Functionality:** Unlike lists, NumPy allows for element-wise (vectorized) operations, meaning you can add or multiply entire arrays without manual loops.



### C. Key Array Attributes
To inspect the structure of data, NumPy provides essential attributes:
* **ndim:** Returns the number of dimensions (axes) of the array.
* **shape:** Returns a tuple indicating the size of the array in each dimension (e.g., `(2, 3)` for 2 rows and 3 columns).
* **dtype:** Describes the data type of the elements (e.g., `int64`, `float64`).

### D. Statistical Insights
NumPy provides functions like `mean()` and `median()` to analyze data distribution. 
> **Note:** When the Mean and Median are the same, the data is generally considered "clean" with no major outliers. A large difference between the two suggests the presence of outliers or skewed data.

---

## 4. Algorithms

### 1. Array Declaration and Inspection
1. Import the `numpy` library using the alias `np`.
2. Create an array using `np.array()` by passing a list or a list of lists.
3. Access `.ndim` to check the dimensionality.
4. Access `.shape` to find the dimensions (rows, columns).
5. Access `.dtype` to verify the data type of the stored elements.

### 2. Specialized Matrix Generation
1. **Zeros Matrix:** Use `np.zeros((rows, cols))` to create an array filled entirely with 0.0.
2. **Ones Matrix:** Use `np.ones((rows, cols))` to create a symmetric or rectangular matrix of 1.0.
3. **Identity Matrix:** Use `np.eye(n)` to create a square matrix of size `n` with 1s on the diagonal and 0s elsewhere.



### 3. Creating Numerical Ranges
1. **Step-based Range:** Use `np.arange(start, stop, step)` to create a sequence with a specific increment.
2. **Linear Spacing:** Use `np.linspace(start, stop, num)` to create `num` samples spaced evenly over the specified interval.

### 4. Vectorized Arithmetic (Broadcasting)
1. Declare an array (e.g., `a` or `b`).
2. Perform a direct arithmetic operation (e.g., `b * 2` or `a + 5`).
3. NumPy automatically applies the operation to every element in the array without requiring a `for` loop.

### 5. Basic Statistical Analysis
1. Use `np.sum()` to calculate the total of all elements.
2. Use `np.max()` and `np.min()` to identify the range of values in the dataset.
3. Use `np.mean()` and `np.median()` to determine the central tendency of the data and check for outliers.

---

## 5. Conclusion
In this experiment, the NumPy library was implemented to handle numerical data efficiently. We successfully performed array declarations, attribute checks, and explored built-in functions for matrix initialization. The experiment demonstrated NumPy's superiority in mathematical operations and statistical analysis compared to standard Python structures.

---
