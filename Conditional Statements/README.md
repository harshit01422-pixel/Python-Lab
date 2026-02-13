Experiment 6: Study of Conditional Statements in Python
Name: Harshit  
PRN: 25070123053  
Batch: A3  

Experiment: Conditional Statements in Python
## Objectives
To understand the syntax and working of if, elif, and else statements in Python.
To implement logical operators (and, or, not) within conditions.
To solve real-world problems like tax calculation, salary slips, grade systems, and date validation using decision-making statements.
## Theory
### 1. Decision Making in Python
Decision-making is a fundamental concept in programming. It allows a program to choose different actions based on different conditions. In Python, this is achieved using conditional statements.
Conditional statements evaluate a condition that results in either True or False. Depending on the result, a particular block of instructions is executed.
### 2. Types of Conditional Statements
(a) Simple if Statement
Used when an action needs to be performed only if a condition is true.
(b) if-else Statement
Used when one action is performed if the condition is true and another action is performed if the condition is false.
(c) if-elif-else Ladder
Used when multiple conditions need to be checked.
The conditions are evaluated one by one. As soon as a condition is true, its corresponding block executes and the rest are skipped.
(d) Nested if Statements
An if statement inside another if statement. Used when a second condition needs to be checked after the first condition is satisfied.
### 3. Logical Operators
Logical operators are used to combine multiple conditions.
AND: Returns true only if both conditions are true.
OR: Returns true if at least one condition is true.
NOT: Reverses the result of a condition.
These operators are especially useful in complex validations such as leap year calculation and date validation.
### 4. Comparison Operators
Comparison operators are used to compare values in conditions:
Greater than
Less than
Greater than or equal to
Less than or equal to
Equal to
Not equal to
These operators form the basis of all decision-making structures.
### 5. Importance of Conditional Statements
Conditional statements are widely used in:
Payroll systems for salary calculation
Banking systems for tax and interest calculation
Academic systems for grade evaluation
Calendar systems for date and leap year validation
Business applications for discount and offer calculations
They help programs make intelligent decisions and respond differently based on user input.
## Algorithms
### 1. Number Nature (Positive/Negative/Zero)
Start.
Input a number n.
If n is greater than 0 → Print "Positive".
If n is less than 0 → Print "Negative".
Otherwise → Print "Zero".
Stop.
### 2. Odd or Even
Start.
Input number n.
If n is divisible by 2 → Print "Even".
Else → Print "Odd".
Stop.
### 3. Greater of Two Numbers
Start.
Input num1 and num2.
If num1 is greater than num2 → Print num1 is greater.
Else → Print num2 is greater.
Stop.
### 4. Largest of Three Numbers
Start.
Input num1, num2, num3.
If num1 is greater than both num2 and num3 → num1 is largest.
If num2 is greater than both num1 and num3 → num2 is largest.
Otherwise → num3 is largest.
Stop.
### 5. Grade & Average Calculation
Start.
Input marks for 5 subjects.
Calculate Average = (Sum of Marks) ÷ 5.
Use conditional ladder to assign grades (O, A+, A, B+, B, or Fail) based on average range.
Stop.
### 6. Leap Year Check
Start.
Input year.
If year is divisible by 4 and not divisible by 100, or divisible by 400 → Leap Year.
Else → Not a Leap Year.
Stop.
### 7. Date Validation & Increment
Start.
Input date in DD, MM, YY format.
Check if month is between 1 and 12.
Check if day is valid according to the month and leap year rules.
If valid:
If it is the last day of the month → Set day to 1 and increment month.
If month exceeds 12 → Set month to 1 and increment year.
Else:
Print "Invalid Date".
Stop.
### 8. Gross Salary Calculation
Start.
Input Basic Salary.
Assign HRA and DA percentages based on salary condition.
Calculate Gross Salary = Basic + HRA + DA.
Display Gross Salary.
Stop.
### 9. Income Tax Calculation
Start.
Input Income.
Apply tax rates based on income slabs:
0% for income below 2.5 Lakhs
5% for income between 2.5–5 Lakhs
20% for income between 5–10 Lakhs
30% for income above 10 Lakhs
Calculate total tax.
Stop.
## Conclusion
Through this experiment, we studied the theoretical concepts behind conditional statements in Python. We understood how decision-making structures work and how logical and comparison operators help in forming complex conditions. These concepts are essential for solving real-world problems and form a strong foundation for advanced programming topics.


