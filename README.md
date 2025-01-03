# Uncommon Python Bug: ZeroDivisionError in Nested Conditional

This repository demonstrates a subtle `ZeroDivisionError` in a Python function.  The error isn't immediately apparent due to the nested `if-elif-else` structure.

## Bug Description

The `function_with_uncommon_error` aims to return either `a`, `b`, or `a/b` based on their values.  However, it fails to handle the edge case where *both* `a` and `b` are 0, leading to a division by zero error. The conditional statements individually handle `a == 0` and `b == 0`, but not the combination.

## Solution

The provided solution adds an explicit check for `a == 0 and b == 0`, preventing the division by zero.

## How to Run

1. Clone the repository.
2. Navigate to the repository directory.
3. Run `python bug.py` to see the original error.
4. Run `python bugSolution.py` to observe the correct, error-free solution.