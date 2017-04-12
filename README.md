# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: *We first find pairs of identical values within each unit. To do this, we first identify potential candidates (boxes with only two digits) and match them in pairs (using sorting and grouping by value). After this, we simply remove the digits of the naked-twin pair from the other boxes in the unit. By repeatedly applying this constraint (along with other ones) until the Sudoku puzzle stops changing, we effectively perform constraint propagation.*

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: *We perform constraint propagation by repeatedly enforcing the strategy rules, reducing the set of possible values toward a possible solution for the Sudoku. To solve the diagonal sudoku problem, we actually do not need to modify the constraint propagation code itself. The reason is simple: the constraint propagation code does not actually care where each unit is located in the puzzle. It only needs to know which units it needs to transform. To add support for the diagonal constraint, we only had to create two additional units that represent the diagonals of the grid.*

### Install

This project requires **Python 3**.

We recommend students install [Anaconda](https://www.continuum.io/downloads), a pre-packaged Python distribution that contains all of the necessary libraries and software for this project. 
Please try using the environment we provided in the Anaconda lesson of the Nanodegree.

##### Optional: Pygame

Optionally, you can also install pygame if you want to see your visualization. If you've followed our instructions for setting up our conda environment, you should be all set.

If not, please see how to download pygame [here](http://www.pygame.org/download.shtml).

### Code

* `solutions.py` - You'll fill this in as part of your solution.
* `solution_test.py` - Do not modify this. You can test your solution by running `python solution_test.py`.
* `PySudoku.py` - Do not modify this. This is code for visualizing your solution.
* `visualize.py` - Do not modify this. This is code for visualizing your solution.

### Visualizing

To visualize your solution, please only assign values to the values_dict using the ```assign_values``` function provided in solution.py

### Data

The data consists of a text file of diagonal sudokus for you to solve.