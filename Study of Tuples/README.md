# Experiment: Study of Tuples in Python
## Title

Study of Tuples in Python

## Aim

To study and understand tuples in Python, their properties, operations, and commonly used tuple functions.

## Objectives

To understand the concept of tuples in Python

To learn how to create and access tuples

To study tuple indexing and slicing

To understand immutability of tuples

To use built-in tuple functions

## Theory
1. Introduction to Tuples

A tuple in Python is a built-in data structure used to store a collection of elements in a single variable.

Characteristics of Tuples:

Ordered collection

Immutable (elements cannot be changed after creation)

Allows duplicate elements

Can store elements of different data types

Example:

my_tuple = (10, 20, 30, "Python", 5.5)

2. Creating Tuples

Tuples are created using parentheses ().

A tuple with multiple elements:

t1 = (1, 2, 3)


A tuple with a single element (comma is mandatory):

t2 = (5,)

3. Accessing Tuple Elements

Tuple elements can be accessed using index values, starting from 0.

Example:

t1[0]    # First element
t1[-1]   # Last element

4. Tuple Indexing and Slicing

Indexing accesses a single element

Slicing accesses a range of elements

Example:

t1[1:4]

5. Tuple Immutability

Tuples are immutable, meaning their elements cannot be modified, added, or removed after creation.

However, tuple elements can be accessed and used in expressions.

6. Built-in Tuple Functions

len() – Returns the number of elements

max() – Returns the maximum element

min() – Returns the minimum element

sum() – Returns the sum of elements

count() – Counts occurrences of an element

index() – Returns index of first occurrence

7. Traversing a Tuple

Tuple elements can be accessed using loops such as a for loop.

Example:

for item in t1:
    print(item)

## Conclusion

Thus, tuples in Python, their properties, indexing, slicing, immutability, and built-in functions were studied and implemented successfully.
