# graphs_llennon

graphs_llennon is a Python library containing graph-related algorithms. The library currently includes an implementation of Dijkstra's shortest path algorithm, which can be used to find the shortest paths from a starting vertex to other vertices in a weighted graph.


Features:
Dijkstra's shortest path algorithm
Calculates the shortest distance from a source vertex to other vertices
Tracks the path used to reach each vertex
Uses a heap-based priority queue
Can be installed as a Python package using pip


Project Structure:
hwk4/
│
├── src/
│   └── graphs_llennon/
│       ├── __init__.py
│       ├── heapq.py
│       └── sp.py
│
├── test.py
├── README.md
└── pyproject.toml


Installation:

  -Clone or download the repository and open a terminal in the project's root directory.
  -Install the package using pip:
  -python -m pip install .
  -For development, the package can also be installed in editable mode:
  -python -m pip install -e .
  -After installation, the package can be imported with:
  -from graphs_llennon import sp


Using the Library:

The Dijkstra algorithm accepts a weighted graph represented as a Python dictionary and a source vertex.

Example:

from graphs_llennon import sp

graph = {
    0: {1: 4, 2: 1},
    1: {3: 1},
    2: {1: 2, 3: 5},
    3: {4: 3},
    4: {4: 0}
}

source = 0

dist, path = sp.dijkstra(graph, source)

print(dist)
print(path)

The dist dictionary contains the shortest known distance from the source vertex to each vertex. The path dictionary contains the vertices used to reach each destination.


Running the Test Program:
The included test.py program reads a graph from a text file and runs Dijkstra's shortest path algorithm.
The graph file should contain one edge per line using the following format:

source destination weight

For example, a file named graph.txt could contain:

0 1 4
0 2 1
1 3 1
2 1 2
2 3 5
3 4 3
4 4 0

Run the test program with:

python test.py graph.txt

The program will display the shortest distances from vertex 0 and the shortest-path information calculated by the algorithm.


Requirements:
Python 3.8 or newer
pip
