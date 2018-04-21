[//]: # (Image References)

[image1]: EightQueens.gif "8-queens puzzle solution"

# Constraint Satisfaction in the N-Queens problem

## Introduction
Constraint Satisfaction is a technique for solving problems by expressing limits on the values of each variable in the solution with mathematical constraints. For example, constraints in [the Sudoku project](https://github.com/ntrang086/sudoku_solver) are enforced implicitly by filtering the legal values for each box, and [the planning project](https://github.com/ntrang086/cargo_planning_search) represents constraints as arcs connecting nodes in the planning graph. In this project we will use [SymPy](http://www.sympy.org/en/index.html), a symbolic math library, to explicitly construct binary constraints and then use Backtracking to solve the N-queens problem (which is a generalization [8-queens problem](https://en.wikipedia.org/wiki/Eight_queens_puzzle)). Using symbolic constraints makes it easier to visualize and reason about the constraints (especially for debugging), but comes with a performance penalty. See the `Sympy_Intro notebook` in the same directory for example code on sympy.

![8-queens puzzle solution][image1]

Briefly, the 8-queens problem asks us to place 8 queens on a standard 8x8 chessboard such that none of the queens are in "check" (i.e., no two queens occupy the same row, column, or diagonal). The N-queens problem generalizes the puzzle to to any size square board.

This project consists of three main steps:

* Step 1: Implement the `NQueensCSP` class to develop an efficient encoding of the N-queens problem and explicitly generate the constraints bounding the solution
* Step 2: Implement the search functions for recursive backtracking
* Step 3: Solve the N-queens problem

## Code

* `AIND-Constraint_Satisfaction.ipynb` - Code to solve the N-queens problem
* `util.py` - Helper code to create constraints and visualize solutions
* `Sympy_Intro.ipynb` - Example code of sympy to show how it works

## Setup

* Python 3
* numpy
* sympy
* matplotlib

## Run
To run any script file, use:

`python <script.py>`

To open a notebook, use:

`jupyter notebook <notebook.ipynb>`
