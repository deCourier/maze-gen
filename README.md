# maze-gen
Intermediate Level Maze generation project written in C
Project uses recursive backtracking in order to generate a mildly complicated and unique pattern of a maze. Frequently implemented with a stack, this approach is one of the simplest ways to generate a maze using a computer. Consider the space for a maze being a large grid of cells (like a large chess board), each cell starting with four walls. Starting from a random cell, the computer then selects a random neighbouring cell that has not yet been visited. The computer removes the wall between the two cells and marks the new cell as visited, and adds it to the stack to facilitate backtracking. The computer continues this process, with a cell that has no unvisited neighbours being considered a dead-end. When at a dead-end it backtracks through the path until it reaches a cell with an unvisited neighbour, continuing the path generation by visiting this new, unvisited cell (creating a new junction). This process continues until every cell has been visited, causing the computer to backtrack all the way back to the beginning cell. We can be sure every cell is visited.

# Things to note
Program will prompt for 3 questions, mainly regarding the rows and columns of the maze, which will determine the size and complexity of it, recommended amount is 5-20 rows/cols as <5 will make it too simple, and >20 might have an integer overflow issue as I set the buffer size to 500. 
Last question is stylization of the program, I have chosen 3 colours for to play around with as I find those colours the most appealing for mazes.

Start grid: Pink in colour
Visited cells: Purple in colour
Current cell: Blue in colour
Exit cell: Red in colour
Pathfinding: Green in colour

I used a struct to generate x,y coordinates for the cells for easier readability as well as refactoring. I had some trouble implementing the push and pop function but in the end I realized it was simply just appending and deleting the first indexes available to the stack.

Future implementations: Using Djikstra's Algorithm to calculate a more efficient path from Home to Exit

Use README.MD for the console commands to run program
