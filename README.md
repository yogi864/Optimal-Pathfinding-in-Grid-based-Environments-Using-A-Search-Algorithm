The A* algorithm is a widely used pathfinding algorithm in computer science and artificial
intelligence. It is an informed search algorithm that efficiently finds the shortest path between
two points on a graph or grid. A* combines the advantages of Dijkstra's algorithm
(guaranteed shortest path) and greedy best-first search (efficiency) by using a heuristic to
guide its search.

1. Class Definitions:
 - `Cell`: Represents a single cell in the grid. Each cell has attributes for its coordinates
(`x`, `y`) and whether it is traversable.
 - `Grid`: Initializes a grid of cells with a specified width and height. It also includes
functions to manipulate individual cells, such as setting them as obstacles or checking
their traversability status.

2. Distance Calculation:
 - `euclidean_distance`: Computes the Euclidean distance between two points in a twodimensional space. It utilizes the Pythagorean theorem to calculate the distance between
pairs of coordinates.

3. A* Search Algorithm:
 - `a_star`: Performs the A* search algorithm to find the optimal path from a starting cell
to a goal cell on the grid. It manages an open set as a priority queue to evaluate nodes
based on their estimated total cost (`f_score`). The algorithm iterates through neighboring
cells, updates the path if a better route is found, and adds unvisited neighbors to the open
set until the goal cell is discovered.

4. Neighborhood Generation:
 - `get_neighbors`: Generates neighboring cells that are traversable and within the grid
boundaries. It searches for cells in the cardinal directions (left, right, top, bottom) relative
to the given cell.

5. Path Reconstruction:
 - `reconstruct_path`: Reconstructs the optimal path from the `came_from` dictionary
generated during A* search. It traces the parent cells backward from the goal cell to the
starting cell.

6. Graphical User Interface (GUI):
 - `main`: Creates an interactive GUI using IPywidgets for users to input grid
dimensions, add obstacles, set start and goal positions, and visualize the pathfinding
process. When the visualize button is clicked, the grid, obstacles, start, goal, and optimal
path are displayed using Matplotlib.
