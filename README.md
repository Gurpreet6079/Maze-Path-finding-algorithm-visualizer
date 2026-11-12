# Maze & Pathfinding Algorithm Visualizer

An interactive Python application that demonstrates how **Breadth-First Search (BFS)** and **Depth-First Search (DFS)** navigate a maze. Build a maze by clicking or dragging across the grid, choose an algorithm, and watch its search process animate from start to finish.

## Objective

This project is designed to make the behavior of fundamental graph-traversal algorithms easy to see and compare. It shows that BFS explores the grid level by level and finds a shortest path in an unweighted grid, while DFS follows a branch deeply before backtracking and does not guarantee the shortest path.

## Features

- Interactive 17 × 25 maze grid
- Click-and-drag wall drawing
- BFS and DFS algorithm selection
- Animated explored cells and final path
- Random maze generation
- Clear-wall and reset controls
- Search status showing path length and number of explored cells
- Start and end cells fixed at opposite corners

## How it works

The grid is treated as a graph:

- Each open cell is a vertex.
- Up, right, down, and left adjacent cells are edges.
- Walls are excluded from traversal.
- A `seen` set prevents revisiting cells.
- A parent map reconstructs the route after the end cell is found.

Both algorithms have time complexity **O(V + E)** and space complexity **O(V)**, where `V` is the number of open cells and `E` is the number of valid neighboring connections.

## Technologies

- Python 3
- Tkinter (Python's built-in desktop GUI library)
- `random` (Python standard library)

No external Python packages, dataset, API key, or internet connection are required.

## Run the project

### Option 1: Run from the notebook

1. Clone or download this repository.
2. Open `Daa project.ipynb` in Jupyter Notebook or JupyterLab.
3. Run the populated code cell.
4. A desktop window titled **Maze & Path Finding Algorithm Visualizer** will open.

### Option 2: Run as a Python script

1. Export the populated notebook cell to a file such as `maze_visualizer.py`.
2. In a terminal in the project folder, run:

```bash
python maze_visualizer.py
```

> Tkinter is included with most standard Python installations. On Linux, install the operating-system package that provides Tkinter (commonly `python3-tk`) if it is missing.

## Using the app

1. Click or drag across open cells to create walls.
2. Select **BFS** or **DFS** from the Algorithm menu.
3. Select **Visualize** to animate the search.
4. Use **Random maze**, **Clear walls**, or **Reset** to begin another experiment.

Color guide: green = start, red = end, dark blue = wall, light blue = explored, yellow = final path.

## Project structure

```text
.
├── Daa project.ipynb    # Main application notebook
├── README.md            # Project overview and usage instructions
└── .gitignore           # Local and generated files excluded from Git
```

## GitHub repository description

Interactive Python Tkinter visualizer for comparing BFS and DFS pathfinding in custom or randomly generated mazes.

## Suggested repository name

`maze-pathfinding-visualizer`

## Notes for contributors

Keep personal machine files, virtual environments, notebook checkpoints, and any locally added datasets out of the repository. This project currently has no secrets or datasets to configure.
