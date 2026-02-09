Experiment 6: Study of Conditional Statements in Python
Name: Harshit
PRN: 25070123053
Batch: A3

## Objectives
To understand the syntax of if, elif, and else in Python.
To implement logical operators (and, or, not) within conditions.
To solve real-world problems like tax calculation, salary slips, and date validation.
## Algorithms
### 1. Number Nature (Positive/Negative/Zero)
Start.
Input a number n.
Check if n > 0: Print "Positive".
Check if n < 0: Print "Negative".
Otherwise: Print "Zero".
Stop.
### 2. Odd or Even
Start.
Input number n.
If n \pmod 2 = 0: Print "Even".
Else: Print "Odd".
Stop.
### 3. Greater of Two Numbers
Start.
Input num1 and num2.
If num1 > num2: Print num1 is greater.
Else: Print num2 is greater.
Stop.
### 4. Largest of Three Numbers
Start.
Input num1, num2, num3.
Compare using logical AND:
If (num1 > num2) and (num1 > num3), num1 is largest.
If (num2 > num1) and (num2 > num3),$num2 is largest.
Else num3 is largest.
Stop.
### 5. Grade & Average Calculation
Start.
Input marks for 5 subjects.
Calculate Average = \frac{\sum Marks}{5}.
Use if-elif ladder to assign grades (O, A+, A, B+, B, or Fail) based on the Average value.
Stop.
### 6. Leap Year Check
Start.
Input year.
If (year % 4 == 0 \text{ and } year % 100 != 0) \text{ or } (year % 400 == 0):
Print "Leap Year".
Else: Print "Not a Leap Year".
Stop.
### 7. Date Validation & Increment
Start.
Input date string, split into DD,MM, YY.
Validate M (1-12) and D based on the specific month and leap year rules.
If valid, check if D is the last day of the month.
If yes: Set D=1, increment M. (If M>12, set M=1, increment Y).
If no: Increment D.
Stop.
### 8. Gross Salary Calculation
Start.
Input Basic.
If Basic = 10,000: HRA=20%, DA=80%.
Else if Basic = 20,000: HRA=25%, DA=90%.
Else: HRA=30%, DA=95%.
Calculate Gross = Basic + HRA + DA.
Stop.
### 9. Income Tax Calculation
Start.
Input Income.
Use conditional slabs:
0% \text{ for } < 2.5L.
5% \text{ for } 2.5L - 5L.
20% \text{ for } 5L - 10L.
30% \text{ for } > 10L.
Stop.
## Conclusion
Through this experiment, we have successfully implemented and analyzed various conditional structures in Python, ranging from simple if-else blocks to complex nested conditions and if-elif-else ladders.


