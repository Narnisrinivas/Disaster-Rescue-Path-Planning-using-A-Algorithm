**Disaster Rescue Path Planning using A* Algorithm**

This project implements the A* (A-Star) Pathfinding Algorithm to help rescue teams find the shortest and safest path during disaster situations such as:
Earthquakes
Floods
Cyclones
Building collapses
In such emergencies, roads may be blocked and time is critical. Our system automatically finds an optimal path from the start location (C) to the target location (T) while avoiding obstacles.

Objective:

The main goal of this project is to:
Represent disaster areas as grid maps
Identify blocked and free paths
Apply the A* algorithm
Compute the shortest rescue path efficiently
Assist emergency response teams in navigation

Algorithm Used:

A* (A-Star) Algorithm
A* is a graph traversal and pathfinding algorithm that calculates the shortest path using:
f(n)=g(n)+h(n)
Where:
g(n) = cost from start node to current node
h(n) = heuristic cost from current node to goal node
f(n) = total estimated cost

Heuristic Function Used:

We used Manhattan Distance:
h(x,y)=∣x1−x2∣+∣y1−y2∣
This works well because movement is allowed only in:
Up
Down
Left
Right

Time Complexity:
O(1)

Data Structures Used:

1. Grid Representation
The environment is represented as a matrix where:
0 → Free cell
1 → Obstacle
C → Start position
T → Target position
Example grid input format:
2. Min Heap (Priority Queue)
Used to manage the open list in A* algorithm.

Operations:

Insert (push)
Best case: O(1)
Worst case: O(log n)
Delete (pop)
Best case: O(1)
Worst case: O(log n)

Working Steps of Algorithm:

Start from source node (C)
Insert node into Min Heap
Select node with lowest f(n)
Explore neighbors (up, down, left, right)
Ignore blocked cells
Update shortest path cost
Repeat until target node (T) is reached
Reconstruct final shortest path

Time Complexity:

Best Case
Goal is close to start:
O(1) to O(log V)

Worst Case
When most nodes are explored:
O(E log V)
Where:
V = number of vertices
E = number of edges

Input Files Included:

The project contains multiple grid test cases:
input1.txt → 10 × 10 grid
input2.txt → 20 × 20 grid
input3.txt → 30 × 30 grid
input4.txt → 40 × 40 grid
input5.txt → 50 × 50 grid
Each file represents different disaster environments with obstacles.

Advantages:

Finds shortest path efficiently
Works well on grid-based maps
Faster than BFS and Dijkstra in many cases
Suitable for rescue operations
Easy to implement and understand

Limitations:

Uses more memory for large grids
Performance reduces for very large maps
Not ideal for extremely large real-time environments

Applications:

This system can be used in:
Disaster rescue navigation
Emergency evacuation planning
Robotics path planning
Game AI movement systems
Smart city rescue systems

Conclusion:

This project demonstrates how the A* algorithm can efficiently determine the shortest rescue path in disaster situations using grid-based obstacle maps. It improves decision-making speed and helps emergency teams reach victims faster.
