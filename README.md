# graphs_llennon

`graphs_llennon` is a Python library that implements Dijkstra's shortest path algorithm for weighted graphs.

## Installation

Install the package from the project directory using pip:

```bash
python -m pip install .
```

## Usage

Import the shortest path module with:

```python
from graphs_llennon import sp
```

Example:

```python
graph = {
    0: {1: 4, 2: 1},
    1: {3: 1},
    2: {1: 2, 3: 5},
    3: {3: 0}
}

dist, path = sp.dijkstra(graph, 0)

print(dist)
print(path)
```

## Testing

The included `test.py` reads a weighted graph from a text file.

Run it with:

```bash
python test.py graph.txt
```

## Project Structure

```text
src/
└── graphs_llennon/
    ├── __init__.py
    ├── heapq.py
    └── sp.py
test.py
README.md
pyproject.toml
```
