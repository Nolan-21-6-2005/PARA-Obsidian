---
title: "Depth First Search (DFS) for Artificial Intelligence"
source: "https://www.geeksforgeeks.org/artificial-intelligence/depth-first-search-dfs-for-artificial-intelligence/"
author:
  - "[[GeeksforGeeks]]"
published: 2024-05-16
created: 2025-10-23
description: "Your All-in-One Learning Portal: GeeksforGeeks is a comprehensive educational platform that empowers learners across domains-spanning computer science and programming, school education, upskilling, commerce, software tools, competitive exams, and more."
tags:
  - "clippings"
---
- [Artificial Intelligence](https://www.geeksforgeeks.org/artificial-intelligence/artificial-intelligence/)
- [Interview Questions](https://www.geeksforgeeks.org/artificial-intelligence/artificial-intelligenceai-interview-questions-and-answers/)
- [Project Ideas](https://www.geeksforgeeks.org/artificial-intelligence/best-artificial-intelligence-project-ideas/)
- [Search Algorithms](https://www.geeksforgeeks.org/machine-learning/search-algorithms-in-ai/)
- [Local Search Algorithm](https://www.geeksforgeeks.org/artificial-intelligence/local-search-algorithm-in-artificial-intelligence/)
- [Generative AI](https://www.geeksforgeeks.org/artificial-intelligence/what-is-generative-ai/)
- [Data Science](https://www.geeksforgeeks.org/data-science/data-science-for-beginners/)
- [Machine Learning](https://www.geeksforgeeks.org/machine-learning/machine-learning/)
- [Deep Learning](https://www.geeksforgeeks.org/deep-learning/deep-learning-tutorial/)
- [ML-Projects](https://www.geeksforgeeks.org/machine-learning/machine-learning-projects/)
- [Robotics](https://www.geeksforgeeks.org/artificial-intelligence/artificial-intelligence-in-robotics/)

[Open In App](https://geeksforgeeksapp.page.link/?link=https://www.geeksforgeeks.org/depth-first-search-dfs-for-artificial-intelligence/?type%3Darticle%26id%3D1233321&apn=free.programming.programming&isi=1641848816&ibi=org.geeksforgeeks.GeeksforGeeksDev&efr=1)

Suggest changes

2 Likes

Like

Report

Depth-First Search (DFS) is a helpful method in artificial intelligence. It helps AI systems work better and faster. DFS gives useful ideas for solving problems and is used in many real-world AI tasks. This article provides insights about what DFS is, why it matters in AI, and where it’s used in practice.

## What is a Depth-First Search in AI?

[Depth-first search](https://www.geeksforgeeks.org/dsa/depth-first-search-or-dfs-for-a-graph/) is a traversing algorithm used in tree and graph-like data structures. It generally starts by exploring the deepest node in the frontier. Starting at the root node, the algorithm proceeds to search to the deepest level of the search tree until nodes with no successors are reached. Suppose the node with unexpanded successors is encountered then the search backtracks to the next deepest node to explore alternative paths.

### DFS Working

Depth-first search (DFS) explores a graph by selecting a path and traversing it as deeply as possible before backtracking.

Search operation of the depth-first search

- Originally it starts at the root node, then it expands its one branch until it reaches a dead end. Then it backtracks to the most recent unexplored node, repeating until all nodes are visited or a specific condition is met. ( As shown in the above image, starting from node A, DFS explores its successor B, then proceeds to its descendants until reaching a dead end at node D. It then backtracks to node B and explores its remaining successors i.e E. )
- This systematic exploration continues until all nodes are visited or the search terminates. (In our case after exploring all the nodes of B. DFS explores the right side node i.e C then F and and then G. After exploring the node G. All the nodes are visited. It will terminate.

## Key characteristics of DFS

In simple terms, the DFS algorithms in [AI](https://www.geeksforgeeks.org/artificial-intelligence/ai-algorithms/) holds the power of extending the current path as deeply as possible before considering the other options.

- ****Not Cost-Optimal****: DFS is not cost-optimal because it does not guarantee finding the shortest path to the goal. It may find a solution quickly, but that path might not be the shortest or the cheapest one.
- ****Stack-Based Search****: DFS uses a stack to remember which nodes to explore next. When DFS visits a new node, it adds it to the stack. It keeps going deeper by exploring neighbors. If it reaches a dead end (a node with no more children), it backtracks by removing nodes from the stack and exploring other possible paths.
- ****Backtracking Search****: A variant of DFS is called backtracking search, which uses less memory. Instead of creating all possible paths at once, it generates one child node at a time. It can also modify the current state directly without making a new copy. This saves memory by only keeping one state and the path taken so far.

## Edge classes in a Depth-first search tree based on a spanning tree

![edge-classes-in-dfs](https://media.geeksforgeeks.org/wp-content/uploads/20240502130628/edge-classes-in-dfs.webp)

Edge classes in DFS based on spanning tree

The edges of the depth-first search tree can be divided into four classes based on the spanning tree, they are

- ****Forward edges:**** The forward edge is responsible for pointing from a ****node**** of the tree to one of its ****successors****.
- ****Back edges:**** The back edge holds the power of directing its edge from a ****node**** of the tree to one of its ****ancestors****.
- ****Tree edges:**** When DFS explores the new vertex from the current vertex, the edge connecting them is called a tree edge. It is essential while constructing a DFS spanning tree because it represents the paths to be followed during the traversal.
- ****Cross edges:**** Cross edges are the edges that connect two vertices that are neither ancestors nor descendants of each other in the DFS tree.

## Depth First Search(DFS) Algorithm in Python

### 1\. Initialization

The graph is stored as a dictionary (adjacency list).

![Screenshot-2025-07-07-115536](https://media.geeksforgeeks.org/wp-content/uploads/20250707150103409216/Screenshot-2025-07-07-115536.png)

Graph for this implementation

We also prepare:

- A set `visited` to track visited nodes.
- A list `traversal_order` to record the DFS path.

```
# Define the graph as an adjacency list
```

```
graph = {
```
```
'A': ['B', 'C'],
```
```
'B': ['D', 'E'],
```
```
'C': ['F'],
```
```
'D': [],
```
```
'E': [],
```
```
'F': []
```
```
}
```
```
​
```
```
visited = set()           # To track visited nodes
```
```
traversal_order = []      # To store DFS traversal result
```

### 2\. Define the DFS Function

This is a recursive DFS function:

- If the node hasn't been visited: Mark it visited, add it to the result and recursively visit all unvisited neighbors

```
def dfs(node):
```

```
if node not in visited:
```
```
visited.add(node)                 # Mark node as visited
```
```
traversal_order.append(node)
```
```
​
```
```
for neighbor in graph[node]:     # Visit all neighbors
```
```
dfs(neighbor)
```

### 3\. Start DFS Traversal from Node 'A'

We start DFS from node A. It will go as deep as possible before backtracking.

```
dfs('A')
```

### 4\. Final Traversal Order

This prints the final DFS order of visited nodes in a depth-first manner.

```
print("\nFinal Traversal Order:")
```

```
print(" → ".join(traversal_order))
```

****Output:****

> Final Traversal Order: A → B → D → E → C → F

> ****You can download the complete code from**** [here](https://media.geeksforgeeks.org/wp-content/uploads/20250708124431963140/DFS_Algorithm_in_Python.ipynb).

## Time complexity of DFS:

### 1\. Explicit Time Complexity

This [time complexity](https://www.geeksforgeeks.org/dsa/time-complexity-and-space-complexity/) arises because DFS traverses each vertex and edge exactly once in the worst-case scenario. This complexity is for explicit traversing of DFS without any repetition. The time complexity of DFS is commonly represented as

> O(|V| + |E|)

Where:

- V: represents the number of vertices,
- E: represents the number of edges.

### 2\. Implicit Time Complexity

This implicit time complexity is appropriate while considering the time complexity in terms of the number of nodes visited in the tree instead of the number of edges and vertices in a graph. For implicit traversing of DFS can be simply depicted as,

> O(b <sup><span>d</span></sup>)

where:

- b: represents the branching factor,
- d: represents the depth of the search.

## Space complexity of DFS

### 1\. Explicit Space Complexity

The [space complexity](https://www.geeksforgeeks.org/dsa/time-complexity-and-space-complexity/) of DFS is commonly represented as

> O(|V|)

Where:

- V: represents the number of vertices.

This is because DFS typically uses additional data structures like stack or [recursion](https://www.geeksforgeeks.org/dsa/introduction-to-recursion-2/) stack to keep track of visited vertices.

### 2\. Implicit Space Complexity

For an implicit search in a graph, DFS’s space complexity can be represented as follows:

> ****O(bd)****

where:

- b: represents the branching factor,
- d: represents the depth of the search.

This space complexity is said to be considered when the space is required to store the nodes on the current path during the search.

## DFS Implementation in Robotics Pathfinding

DFS can be used to find a path from a start node to a goal node in a maze or grid-based environment. The DFS algorithm systematically explores all possible paths from the start node, one branch at a time until it finds a path that leads to the goal. The below figures show the maze which contains the initial state of the robot, the obstacles, and the goal state. Here, the goal node is in the position of (0,5) where the robot needs to traverse through the maze to find the path to reach the goal.

### Step 1: Define Maze dimensions and obstacles

We define a ****maze\_size**** representing the dimension of the maze, in our case, it's a 6x6 grid. A [list](https://www.geeksforgeeks.org/cpp/list-cpp-stl/) of coordinates that represents the positions of obstacles within a maze is also specified. The robot is positioned at the initial state (0,0) and aims to reach the goal state (0,5).

![Maze environment -Geeksforgeeks](https://media.geeksforgeeks.org/wp-content/uploads/20240502130733/path-finding-in-dfs-(2).webp)

Maze environment

****Maze dimensions and obstacles****

```
# Maze dimensions and obstacles
```

```
maze_size = 6
```
```
obstacles = [(0,1),(1,1),(3,2),(3,3),(3,4),(3,5),(0,4),(4,1),(4,2),(4,3)]
```
```
start = (0,0)
```
```
goal = (0,5)
```

### Step 2: Define a is\_valid function

The ****is\_valid**** function checks whether a given position of (x,y) is valid such that it inspects that it's within the bounds of the maze and not obstructed by any obstacles.

```
def is_valid(x,y):
```

```
return 0 <= x < maze_size and 0 <= y < maze_size and (x,y) not in obstacles
```

### Step 3: Define dfs function (Depth-first search):

In the below code, we define the dfs function to implement the DFS algorithm. It uses a stack to keep a record of the nodes it visits, and it iterates through each node that helps in exploring its neighbors recursively until it finds the goal node or it exhausts all possibilities.

- The empty stack stores nodes to be explored, and the empty [set](https://www.geeksforgeeks.org/cpp/set-in-cpp-stl/) is used to keep track of nodes that have been already visited to avoid revisiting them.
- If the current node is found to be the goal node, it reverses the path so that the robot can follow and it finally returns ****"Path found"****.
- If no path is found, it returns ****"No path found"****. This is an exhaustive search approach, it ensures that all the potential paths are explored and provides a comprehensive solution to the maze-navigating problem.
`  ``` def dfs (current, visited, path):   x, y = current   if current == goal:     path.append(current)     return True   visited.add(current)   moves = [(x-1,y), (x+1, y), (x, y-1), (x, y+1)]   for move in moves:     if is_valid(*move) and move not in visited:       if dfs(move, visited, path):         path.append(current)         return True   return False ```  `

### Step 4: Call DFS function to find the path

`  ``` #Call DFS function to find the path visited = set() path = [] if dfs(start, visited, path):   path.reverse()   print("Path found:")   for position in path:     print(position) else:   print("No path found!") ```  `

****Output:****

> Path found:  
> (0, 0)  
> (1, 0)  
> (2, 0)  
> (3, 0)  
> (3, 1)  
> (2, 1)  
> (2, 2)  
> (1, 2)  
> (0, 2)  
> (0, 3)  
> (1, 3)  
> (2, 3)  
> (2, 4)  
> (1, 4)  
> (1, 5)  
> (0, 5)

****Output explanation****

- ****Step 1:**** We first start at the initial position (0,0), it is where the robot begins its exploration.
- ****Step 2:**** The robot moves right along the top row of the maze such as (1,0), (2,0),(3,0).
- ****Step 3:**** Now, the robot moves down to the second row to the position of (3,1).
- ****Step 4:**** The robot follows a path to the left (2,1), then down (2,2), then right (1,2), and then down again (0,2).
- ****Step 5:**** Now, the robot moves right to reach the third row to the position (0,3).
- ****Step 6:**** The robot moves right along the third row such as passing the positions of (1,3) and (2,3).
- ****Step 7:**** The robot moves down to the fourth row (2,4) and then it moves left (1,4).
- ****Step 8:**** The robot moves right to the last column (1,5).
- ****Step 9:**** Finally, the robot reaches the goal node at the bottom-left corner(0,5) of the maze.
![path-finding-in-dfs-final-output](https://media.geeksforgeeks.org/wp-content/uploads/20240502130855/path-finding-in-dfs-final-output.webp)

Output representation

> ****You can download the complete code from**** [here](https://media.geeksforgeeks.org/wp-content/uploads/20250708124524966183/Robots_Pathfinding_DFS.ipynb).

## Applications of DFS in AI

- ****Maze generation:**** The Maze generation is comprised of designing a layout of passages and walls within a maze. This maze generation makes use of a randomized approach of the Depth-first search algorithm because it leverages the recursive method and stack. For instance, assume that the space is a large grid of cells where each cell holds the four walls. The DFS performs by selecting any random neighbor at first that has not been visited. It removes the wall between the two cells that are not connected and then it adds the new cell to the stack. This process continues until there is no more solution can be generated, resulting in a complete maze.
- ****Puzzle-solving:**** Puzzle-solving including Japanese nonograms can employ Depth-first search as a method for systematically exploring possible solutions. In Japanese nonograms, DFS is utilized to explore different combinations of filled and empty cells in the grid.
- ****Pathfinding in robotics:**** DFS can be employed for pathfinding in robotics, especially in scenarios where simplicity, memory efficiency, and adaptability are important considerations.
  [T](https://www.geeksforgeeks.org/user/tejashreeganesan/)

[tejashreeganesan](https://www.geeksforgeeks.org/user/tejashreeganesan/)

Improve

### Explore

## Introduction to AI

## AI Concepts

## Machine Learning in AI

## Robotics and AI

## Generative AI

## AI Practice

Login Modal | GeeksforGeeks