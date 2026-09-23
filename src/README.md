# Lab Reflection: Git Version Control + Debugging (BuggyProgram)



## Student Name

Bernard Thomas Kelly



## GitHub Repository URL

https://github.com/pagetablemasking/Unit8_lab1



---

# Commit 1: Initial Commit

## What did you include in this commit?
The starter files for the `unit8_lab1` project, including `BuggyProgram.java`, `README.md`, and the three JUnit test classes

## What was the purpose of this commit?
To establish the baseline version of the project in version control before making any logical changes or fixes to the buggy methods.


---



# Commit 2: Task 1 (getGrade)

## Which tests in Task1Test were failing before your fix?
Tests evaluating scores above 90 and between 81-90.

## What was the issue in the code?
The original string returns were swapped. A score above 90 incorrectly returned "Meets", while a score above 80 returned "Exceeds".

## What change did you make to fix it?
I updated the conditional branches to return the performance levels from highest to lowest. Scores > 90 now return "Exceeds", > 80 return "Meets", and everything else defaults to "Does Not Meet". I also flattened the nested `else { if () }` into a cleaner `else if` structure.

## How did the tests help guide your fix?
The failed test assertions immediately highlighted the logical mismatch between the expected category and the actual string returned.


---



# Commit 3: Task 2 (sumEvenNumbers)



## Which tests in Task2Test were failing before your fix?

-



## What was the issue in the code?

-



## What change did you make to fix it?

-



## How did the tests help guide your fix?

-



---



# Commit 4: Task 3 (sumRange)



## Which tests in Task3Test were failing before your fix?

-



## What was the issue in the code?

-



## What change did you make to fix it?

-



## How did the tests help guide your fix?

-



---



# Overall Reflection



## Which task was the easiest to fix? Why?

-



## Which task was the most difficult? Why?

-



## How did Git help you track your progress through the debugging process?

-



## Why is it important to make small, frequent commits when debugging code?

-



## What did you learn about using JUnit tests to guide debugging?

-



---



# Commit 5: Final Reflection



## What did you complete or update before making this final commit?

-



## Why is it useful to document your work after completing a programming task?

- 

