# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: Given two boxes that are considered _naked twins_ for a partially solved sudoku puzzle. We can create a second **elimination strategy** where, for each peer of the provided twins, we eliminate the digits belonging to these peers.

The **naked twin strategy** becomes another **constrain**, avoiding the investigation os possilibity trees without a solution (during `search` execution). Consequently the `solve` method always converge and in a faster pace.

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: Both ascending and descending diagonals can be considered units. Consequently, when the elimination strategies are executed on a box which belongs to the diagonals, the elimination becomes even more restrictive increasing the search algorithm conversion.

### Install

This project requires **Python 3**.

We recommend students install [Anaconda](https://www.continuum.io/downloads), a pre-packaged Python distribution that contains all of the necessary libraries and software for this project. 
Please try using the environment we provided in the Anaconda lesson of the Nanodegree.

##### Optional: Pygame

Optionally, you can also install pygame if you want to see your visualization. If you've followed our instructions for setting up our conda environment, you should be all set.

If not, please see how to download pygame [here](http://www.pygame.org/download.shtml).

### Code

* [`solution.py`](solution.py): You'll fill this in as part of your solution.
* [`test_solution.py`](tests/test_solution.py): Do not modify this. You can test your solution by running `python -m unittest`.
* [`PySudoku.py`](PySudoku.py): Do not modify this. This is code for visualizing your solution.
* [`visualize.py`](visualize.py): Do not modify this. This is code for visualizing your solution.

### Visualizing

To visualize your solution, please only assign values to the values_dict using the `assign_value` function provided in solution.py

### Submission
Before submitting your solution to a reviewer, you are required to submit your project to Udacity's Project Assistant, which will provide some initial feedback.  

The setup is simple.  If you have not installed the client tool already, then you may do so with the command `pip install udacity-pa`.  

To submit your code to the project assistant, run `udacity submit` from within the top-level directory of this project.  You will be prompted for a username and password.  If you login using google or facebook, visit [this link](https://project-assistant.udacity.com/auth_tokens/jwt_login) for alternate login instructions.

This process will create a zipfile in your top-level directory named sudoku-<id>.zip.  This is the file that you should submit to the Udacity reviews system.

