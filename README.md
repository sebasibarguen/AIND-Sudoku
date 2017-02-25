# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: *Student should provide answer here*

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: *Student should provide answer here*

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



### Questions

#### How do we apply constraint propagation to solve the naked twins problem?
To solve the naked twin problem, the basic algorithm is, starting with a box with 2 values,
look for a peer box that has the same values. After knowing which boxes are "naked twins",
you propagate the constraints to all the other boxes in the same unit as the naked twin pairs.
Which means you remove the digits that are in the naked twins from all the other boxes in the
same unit.


#### How do we apply constraint propagation to solve the diagonal sudoku problem?
To solve the diagonal sudoku, it's the same principles as a normal sudoku, with two
additional units, which are the two diagonal lines. The algorithms actually don't change,
the only thing that changes is the additional units for the diagonals. The constraint propagation
then is doing `eliminate`, `only_choice` and `naked_twins` for all units, including the two diagonals.
