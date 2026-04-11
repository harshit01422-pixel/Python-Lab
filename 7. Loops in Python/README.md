#  Study of Loops in Python

## 1. Aim
To study and implement control flow structures (While and For loops) in Python to solve various computational and mathematical problems.

## 2. Objectives
* To understand the syntax and application of `while` and `for` loops.
* To learn loop control statements: `break`, `continue`, and `else`.
* To implement mathematical algorithms like Factorial, Fibonacci, and Prime checks.
* To utilize nested loops for matrix operations and pattern generation.

---

## 3. Theory

### A. Introduction to Loops
In Python, loops are used to execute a block of code repeatedly as long as a certain condition is met. They are essential for automating repetitive tasks and iterating over data structures.

### B. The While Loop
The `while` loop is characterized as an "entry-controlled" loop. It is primarily used when the number of iterations is not known beforehand.
* **Syntax:** `while condition: statement(s)`.
* **Logic:** The condition is evaluated before each iteration. If it evaluates to `True`, the code block executes. If `False`, the loop terminates.

### C. The For Loop
The `for` loop is used for "definite iteration," meaning the number of repetitions is usually determined by the length of a sequence or a range.
* **Range Function:** Often used to generate a sequence of numbers (e.g., `range(1, 7)` prints numbers 1 to 6).
* **Nested Loops:** These involve placing one loop inside another, commonly used for multidimensional data like matrices (3x3).

### D. Loop Control Statements
These statements change the execution from its normal sequence:
* **Break:** Immediately terminates the current loop and resumes execution at the next statement outside the loop.
* **Continue:** Skips the remaining code inside the current iteration and jumps back to the top of the loop to check the condition for the next cycle.
* **Else with Loops:** An `else` block can be used with loops; it executes only if the loop finishes naturally without being interrupted by a `break` statement.

---

## 4. Algorithms for All Implementations

### I. While Loop & Control Algorithms

**1. Basic Iteration (1 to 5)**
1. Initialize counter `i = 1`.
2. While `i <= 5`: Print `i` and increment `i` by 1.

**2. Factorial of a Number**
1. Input number `n` and initialize `fact = 1`.
2. While `n >= 1`: Multiply `fact` by `n` and decrement `n`.
3. Print the final `fact`.

**3. Fibonacci Series**
1. Input terms `n`; initialize `a = 0`, `b = 1`, `i = 0`.
2. While `i < n`: Print `a`, calculate `c = a + b`, set `a = b`, `b = c`, and increment `i`.

**4. Reverse a Number**
1. Input `num`; initialize `rev = 0`.
2. While `num > 0`: Get `digit = num % 10`, update `rev = rev * 10 + digit`, and set `num //= 10`.

**5. Palindrome Check**
1. Input a string or number.
2. Reverse the string using slicing `[::-1]`.
3. If the original matches the reverse, print "Palindrome".

**6. Count Digits**
1. Input `num`; initialize `count = 0`.
2. While `num > 0`: Increment `count` and update `num //= 10`.

**7. Break Function (Exit when i = 3)**
1. Initialize `i = 1`.
2. While `i < 6`: Print `i`. If `i == 3`, execute `break` to exit. Otherwise, increment `i`.

**8. Search in List (With Else)**
1. Define a list and input a target value.
2. Use a while loop to check each index. If found, print the index and `break`.
3. If loop finishes without `break`, the `else` block prints "Not found".

**9. Continue Function (Skip 5)**
1. Initialize `i = 1`. While `i <= 10`:
2. If `i == 5`: Increment `i` and execute `continue` to skip printing.
3. Else: Print `i` and increment `i`.

**10. Print Odd Numbers (1-10 using Continue)**
1. While `i <= 10`: If `i % 2 == 0`, increment `i` and `continue`.
2. Else: Print `i` and increment `i`.

### II. For Loop Algorithms

**11. Sum of first N Numbers**
1. Input `n`. For `i` in `range(1, n+1)`, add `i` to `sum`.

**12. Matrix Multiplication (3x3)**
1. Input elements for 3x3 matrices `A` and `B`.
2. Nest loops: `i` (rows of A), `j` (cols of B), and `k` (shared dimension).
3. Update `result[i][j] += A[i][k] * B[k][j]`.

**13. Possible Digit Combinations**
1. Input three digits into a list.
2. Triple-nest loops `i`, `j`, `k` through the list.
3. If `i`, `j`, and `k` are unique indices, print the combination.

**14. Armstrong Number**
1. For each digit in string `n`: Add `digit ** length_of_n` to a `total`.
2. If `total == n`, it is an Armstrong number.

**15. Prime Number Check**
1. For `i` in `range(2, n)`: If `n % i == 0`, set `flag = 0` and `break`.
2. If the loop completes without finding a divisor, set `flag = 1`.

---

## 5. Pattern Algorithms (Nested Loops)

**1. Inverted Pyramid:** For row `i` in `range(n)`, print `i` spaces and `n-i` stars.
**2. Right Triangle:** Iterate `i` from 0 to `n`; print `*` multiplied by `i`.
**3. Floyd’s Triangle:** Nested loops print a counter `a` that increments after every print.
**4. Number Triangle:** Outer loop `i` prints the value of `i`, `i` times in each row.

---

## 6. Conclusion
Thus, the concepts of loops in Python, their creation, control mechanisms (`break`/`continue`), and implementation in mathematical and matrix logic were studied and implemented successfully.
