# Minimax-Checkers
Project 2 for CISC 3410

Checkers py-game was implemented by Prof. Santhalingam @ CUNY Brooklyn College

Must have py-game library installed to run:
```
pip install pygame
```
The goal of the project was to implement the min_value(), max_value(), and evaluation_function() algorithms, in hopes of making the opponent Agent a better player. 

min_value() and max_value() utilize alpha-beta pruning to eliminate any unsuccessful branches of the minimax tree to save computation time.
#### evalutation_function() explanation:

There are two evaluation functions that are implemented to decide the heuristic for each agent. Blue uses the prewritten heuristic of valuing the capture of Red’s pawns and kings. However, Red uses an added evaluation of primarily focusing on moving its own pieces towards the middle of the board. This is done by adding another function called controlling_center(), which is used to calculate the distance of a piece to the center of the board. The more pieces red has towards the center of the board, the more of a bonus Red will receive. What’s measured is the euclidean distance between a piece and the center of the board. I chose this as an evaluation since in most tabletop games where you must capture the other opponents pieces, controlling the center of the board means winning or losing the game. 

After every move thats made, the time it took for the turn is printed to the console. I found that in more cases it takes a long time for red to find the move it wants to make. This can be due to the circumstances of it's turn it has to deal with or because of the added step within it's evaluation function.

### Future updates:
  I will be looking for solutions to make the implementaion faster, as the program is on the borderline of crashing after every move.
  - Possibility of multi-threading. Will allow the program to run on multiple threads on the machine to get maximum use of the CPU, thus reducing computation time.
  - Possibily adjust the evaluation_function() to me more space efficient when it's used.
  - Add more heuristics to the evaluation function on RED to make it the ultimate checkers champion.
