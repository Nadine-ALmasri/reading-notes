## Graph Basics:

- A graph is a non-linear data structure consisting of vertices (nodes) connected by edges.
- Each vertex can have zero or more adjacent vertices.
- Edges represent connections between vertices.
## Vertex:

- A data object within a graph, also known as a node.
- Can have neighbors, which are other vertices connected by edges.
## Edge:

Represents a connection between two vertices in a graph.
## Degree:

The degree of a vertex is the number of edges connected to that vertex.
## Directed vs. Undirected:

- Undirected Graph: Edges have no direction; connections are bi-directional.
- Directed Graph (Digraph): Edges have direction; each points from one vertex to another.
## Complete vs. Connected vs. Disconnected:

- Complete Graph: All vertices are connected to every other vertex.
- Connected Graph: Every vertex has at least one edge.
- Disconnected Graph: Some vertices may have no edges.
## Acyclic vs. Cyclic:

- Acyclic Graph (DAG): A directed graph without cycles (no repeated paths leading to the same node).
- Cyclic Graph: Contains cycles (paths leading back to the same node).
## Graph Representation:

- Two common representations: Adjacency Matrix and Adjacency List.
- Adjacency Matrix: A 2D Boolean array where rows and columns represent vertices, with 1s indicating edges.
- Adjacency List: A collection of linked lists or arrays, where each vertex stores its connected vertices.
## Weighted Graphs:

- Weighted Graph: Edges have weights (numbers) assigned to them.
- Weighted graphs are used to represent scenarios where connections have different costs or values.
## Graph Traversals:

- Breadth-First Traversal: Visit all nodes closest to the root before moving to the next level.
- Depth-First Traversal: Explore as far as possible along each branch before backtracking.
## Real-World Uses:

- GPS and Mapping: Finding routes and directions.
- Social Networks: Representing relationships between users.
- Airline Traffic: Modeling flight connections.
- Recommendation Systems: e.g., Netflix uses graphs for content recommendations.



Graphs are a fundamental data structure with various applications in computer science and real-world scenarios. Understanding their properties and traversal techniques is crucial for solving complex problems and optimizing algorithms.