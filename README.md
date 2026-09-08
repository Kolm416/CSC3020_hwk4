# graphs_llennon

`graphs_llennon` is a Python library that implements Dijkstra's shortest path algorithm for weighted graphs.

## Installation

Install the package using pip:

```bash
python -m pip install .
```

## Usage

Import the package with:

```python
from graphs_llennon import sp
```

## Testing

Before running `test.py`, create a file named `graphs.txt` in the project folder.

The file should contain the source vertex, destination vertex, and weight for each edge:

```text
0 1 4
0 2 1
1 3 1
2 1 2
2 3 5
3 4 3
4 4 0
```

Then run:

```bash
python test.py graphs.txt
```

The program will use Dijkstra's algorithm to display the shortest distances and paths from vertex `0`.

## Project Structure

```text
hwk4/
├── src/
│   └── graphs_llennon/
│       ├── __init__.py
│       ├── heapq.py
│       └── sp.py
├── graphs.txt
├── test.py
├── README.md
└── pyproject.toml
```
