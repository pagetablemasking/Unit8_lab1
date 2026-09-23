# Lab Reflection: Git Version Control + Debugging (BuggyProgram)



## Student Name

Bernard Thomas Kelly



## GitHub Repository URL

https://github.com/pagetablemasking/Unit8_lab1



---

# Commit 1: Initial Commit

## What did you include in this commit?
The starter files for the `unit8_lab1` project, including `src/BuggyProgram.java`, `README.md`, and the three JUnit test classes

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
All tests verifying the correct sum of even numbers and tests handling standard array boundaries.

## What was the issue in the code?
There were two issues. First, the accumulator variable `sum` was initialized to 1 instead of 0, throwing off every calculation. Second, the `for` loop condition used `<=` instead of `<` against `values.length`, which causes an `ArrayIndexOutOfBoundsException` when the loop attempts to access an index outside the array's bounds.

## What change did you make to fix it?
I changed `int sum = 1;` to `int sum = 0;` and updated the loop boundary to `i < values.length`.

## How did the tests help guide your fix?
The test errors explicitly pointed out the out-of-bounds exception, while the sum verification tests failed by an offset of 1, pointing directly to the initialization error.

---



# Commit 4: Task 3 (sumRange)

## Which tests in Task3Test were failing before your fix?
Tests evaluating a range where the `start` parameter was mathematically greater than the `end` parameter.

## What was the issue in the code?
The `for` loop initialized `i` to `start` and only ran while `i <= end`. If `start` was larger than `end`, the loop bypassed execution entirely and returned a sum of 0, failing to calculate a value across the given range of numbers[cite: 17].

## What change did you make to fix it?
I added a simple conditional swap at the beginning of the method. If `start > end`, the method uses a temporary variable to swap the bounds before executing the loop.

## How did the tests help guide your fix?
The failing tests showed an expected calculated sum but an actual return value of 0, indicating the loop was being skipped entirely due to inverted bounds.

---



# Overall Reflection

## Which task was the easiest to fix? Why?
Task 1 (`getGrade`) was the most straightforward because it simply required reordering string return values to match the instructions. The syntax itself was fully functional.

## Which task was the most difficult? Why?
Task 2 (`sumEvenNumbers`) required the most attention because it contained two separate bugs in a single method. Diagnosing both an initialization error and an off-by-one runtime exception required looking at different types of test failures.

## How did Git help you track your progress through the debugging process?
It isolated each task into a distinct logical change. Troubleshooting code feels very similar to diagnosing a faulty network link or an aircraft component—isolating variables one at a time is the only reliable way to pinpoint the root cause without breaking something else.

## Why is it important to make small, frequent commits when debugging code?
Frequent commits act as safety nets. If a new fix introduces a cascading error elsewhere in the program, a recent, small commit allows you to roll back immediately to a stable state rather than untangling a massive block of uncommitted changes.

## What did you learn about using JUnit tests to guide debugging?
JUnit tests eliminate the guesswork by defining the exact expected behavior against boundaries and edge cases. They act as automated blueprints for how the code should perform under stress.

 

---



# Commit 5: Final Reflection

## What did you complete or update before making this final commit?
I finished answering all the prompt questions in the Overall Reflection section of this README.

## Why is it useful to document your work after completing a programming task?
Thorough documentation ensures that future developers (or yourself months down the line) understand the intent behind a fix, not just the syntax. It serves as a permanent, searchable log of decisions made and problems solved.

