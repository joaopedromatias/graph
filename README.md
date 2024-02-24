# Graphs

G = { V , E }

G = graph
V = vertices
E = edges (connected vertices)

There are two main ways to implement graphs in code:

1. Adjacency List
2. Adjacency Matrix

## Adjacency List

List of vertices, in which it vertices contains a list of its neighbours (representing its edges)

A -> B, C
B -> A, D
...

### Adjacency Matrix

Every vertex is a row and a column heading in a grid (two-dimensional vector). The intersection of a row and column represents if an edge exists between those vertices and the weight of the edge.

For non-directed graphs, the matrix is simetric over its main diagonal, since the relation of vertex A to B is the same of vertex B to A. In this scenario, half of the memory usage is waste.

## Traversing a Graph

There are two ways to do it:

1. Depth First
2. Breadth First

### Depth First

Follows an edge path from a starting vertex until there is no more unvisited vertices in any edge. Then it comes back the path looking for a new edge to visit. It can be implemented using a stack and the visited property of the vertex.

### Breadth First

Starts at the first vertex and visits all vertices connected to this vertex, and then evaluates its connected vertices at the same way. It can be implemented using a `queue` and the visited property of the vertex.

- Example of an adjacency matrix representing a graph

```js
/*
[
  [ 0, 0, 5, 0, 7 ],
  [ 0, 0, 3, 0, 2 ],
  [ 5, 3, 0, 0, 0 ],
  [ 0, 0, 0, 0, 8 ],
  [ 7, 2, 0, 8, 0 ]
]
*/
```

- Visual representation of a graph, containing vertices values and their indexes

```js
/*
    10(0) ----- 7(4) ----- 3(3)
    |            |
    |            |
    |            |
    17(2) ---- 22(1)
*/
```
