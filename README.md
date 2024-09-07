# Sudoku Solver

This Python program solves a 9x9 Sudoku puzzle using a backtracking algorithm. The program takes an unsolved Sudoku grid as input and fills in the missing numbers to provide the completed solution.

## Features

- **Sudoku Puzzle Input**: Predefined unsolved 9x9 Sudoku grid with empty spaces represented by `0`.
- **Backtracking Algorithm**: The program uses a backtracking technique to try possible solutions for each empty cell and finds the correct numbers.
- **Grid Validation**: The `is_valid()` function ensures that no number is repeated in any row, column, or 3x3 sub-grid.
- **Printable Grid**: The solution is displayed in a formatted 9x9 grid.

## How It Works

1. **Check Validity**: Before placing a number in a cell, the program checks if it is valid within the row, column, and 3x3 sub-grid.
2. **Backtracking**: If the number is valid, the program proceeds to the next empty cell. If no valid number can be placed, it backtracks to the previous cell and tries a different number.
3. **Completion**: When the grid is fully solved, the program prints the solved Sudoku puzzle.

## Functions Overview

- **`is_valid(board, row, col, num)`**: Checks if placing a number in a specific cell is valid.
- **`solve_sudoku(board)`**: Recursively tries to solve the Sudoku puzzle using backtracking.
- **`print_board(board)`**: Prints the 9x9 Sudoku grid, formatting it with separators for the sub-grids.

## Example

Input unsolved Sudoku grid:

```bash
5 3 0 0 7 0 0 0 0
6 0 0 1 9 5 0 0 0
0 9 8 0 0 0 0 6 0
8 0 0 0 6 0 0 0 3
4 0 0 8 0 3 0 0 1
7 0 0 0 2 0 0 0 6
0 6 0 0 0 0 2 8 0
0 0 0 4 1 9 0 0 5
0 0 0 0 8 0 0 7 9

Solved Sudoku grid output:
5 3 4 | 6 7 8 | 9 1 2
6 7 2 | 1 9 5 | 3 4 8
1 9 8 | 3 4 2 | 5 6 7
- - - - - - - - - - - -
8 5 9 | 7 6 1 | 4 2 3
4 2 6 | 8 5 3 | 7 9 1
7 1 3 | 9 2 4 | 8 5 6
- - - - - - - - - - - -
9 6 1 | 5 3 7 | 2 8 4
2 8 7 | 4 1 9 | 6 3 5
3 4 5 | 2 8 6 | 1 7 9
