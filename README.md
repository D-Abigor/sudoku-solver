# sudoku-solver
solving sudoku puzzles as part of our computer project for 2023-2024 year

terms used:
#matrix = matrix is defined as the 3x3 square boxes in the puzzle with the restriction of having only 1->9 elements where none of the elements are repeated
#location = location is the location at which an element sits and is represented as a string of length 2 containing the row and column index at positions 0 and 1 of location respectively with respect to the rowlist in the program
#element = elements are the numbers from 1->9 which are used to fill the slots in the puzzle
#slot(s) = slots are the smallest unit boxes in the puzzle which can be filled or which already contains an element in it
#collision = collision is when a given element is already part of its respective row/column/matrix which is against the rules of the puzzle
#compaitable = such a way that no collisions occur


program works by appending the possible elements at a location to a dictionary which we refer to as the core. the core is updated through a series of algorithms which check for compaitable elements at the given location. on each solving run, core is traversed and at each locations where only a single element can be reside it becomes clear that we have a solution for that particular location and the puzzle is updated irreversibly.

compared to using a backtracking algorithm, we have gone with constraint propogation. which makes it unreliable and somewhat complicated but more.. natural.

## current restrictions 
-  the program currently does not have algorithms to handle naked pairs and other advanced methods to solve sudoku
-  the "core" is re initiated on each run, which makes the program repettiive and inneficient.


## improvements
- Add more functionalities where we provide hints and solve the puzzle step by step and indication on how we solved it.
- seperate GUI code from the actual program ( was unaware at the time of building this program that QT5 GUI elements can be imported and dont need to be baked into the code )
