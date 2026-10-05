# N-Queens Problem

## Description

This Python program solves the **N-Queens Problem** using the **Backtracking Algorithm**.

The N-Queens Problem is a classic computer science problem where we need to place **N queens on an N × N chessboard** such that no two queens can attack each other.

Two queens cannot be placed in the same:

* Row
* Column
* Diagonal

The program finds **all possible solutions** for the given value of N.

## Algorithm Used

The program uses **Backtracking**.

Backtracking works by:

1. Placing a queen in a safe position.
2. Moving to the next row.
3. Checking whether the next position is safe.
4. If no safe position is available, going back to the previous row.
5. Moving the previous queen to another position.
6. Continuing until all possible solutions are found.

## How the Program Works

The program uses three sets to keep track of positions that are already occupied:

* `cols` – Stores columns that already contain a queen.
* `diag1` – Stores the values of `row - column` for occupied diagonals.
* `diag2` – Stores the values of `row + column` for occupied diagonals.

The chessboard is represented using a 2D list.

A `"Q"` represents a queen and `"."` represents an empty position.

## Main Function

```python
def solve(n:int):
```

The `solve()` function takes the number of queens `n` as input and returns all possible solutions.

## Backtracking Function

```python
def backtrack(r:int):
```

This recursive function attempts to place a queen in each row.

When `r == n`, all queens have been successfully placed, so the current board configuration is stored as a solution.

## Safety Check

Before placing a queen, the program checks:

```python
if c in cols or (r-c) in diag1 or (r+c) in diag2:
    continue
```

This ensures that the queen does not share a column or diagonal with another queen.

## Example

For:

```python
n = 8
```

the program solves the **8-Queens Problem**.

The number of solutions is:

```text
Total solutions for N =8:92
```

One possible solution is:

```text
Q.......
....Q...
.......Q
.....Q..
..Q.....
......Q.
.Q......
...Q....
```

`Q` represents a queen and `.` represents an empty square.

## Sample Output

```text
Total solutions for N =8:92
one solution:
Q.......
....Q...
.......Q
.....Q..
..Q.....
......Q.
.Q......
...Q....
```

## Requirements

* Python 3.x
* No external libraries are required.

## How to Run

1. Save the program as:

```text
n_queens.py
```

2. Open Command Prompt or Terminal.
3. Navigate to the folder containing the file.
4. Run:

```bash
python n_queens.py
```

## Time Complexity

The N-Queens problem has a high computational complexity because the program explores many possible arrangements.

The approximate time complexity is:

```text
O(N!)
```

The actual execution time depends on the value of N.

## Space Complexity

The program uses the chessboard, sets, recursion stack, and storage for solutions.

Approximate auxiliary space complexity is:

```text
O(N)
```

excluding the space required to store all solutions.

## Concepts Used

* Python Functions
* Recursion
* Backtracking
* Sets
* 2D Lists
* Nested Functions
* Conditional Statements
* Loops
* List Comprehension

## Key Learning

This program demonstrates how **backtracking** can be used to solve constraint-based problems by trying possible choices and undoing a choice when it leads to an invalid solution.

## Author

Created as a Python implementation of the classic **N-Queens Backtracking Problem**.
