Here's the updated README that includes the information from all three sections:

---

# Enhanced-RRT-Algorithm-with-Path-Expansion-Heuristic-Sampling-for-Robot-Path-Planning

## Project Structure

### Main Scripts

- `ep_rrt_star_cluster.py`: Implements the EP-RRT algorithm for a clustered map with square obstacles.
- `ep_rrt_star_general.py`: Implements the EP-RRT algorithm for a general map with different geometric shapes as obstacles.
- `ep_rrt_star_maze_map.py`: Implements the EP-RRT algorithm for a maze-like environment with rectangular and square obstacles.
- `rrt_cluster.py`: Implements the RRT* algorithm in a clustered environment with random square obstacles.
- `rrt_general.py`: Implements the RRT* algorithm in a general environment with predefined obstacle shapes like rectangles, hexagons, and walls.
- `rrt_maze.py`: Implements the RRT* algorithm in a maze-like environment with complex obstacles.
- `rrt_narrow.py`: Implements the RRT* algorithm in a narrow passage environment with tight spaces and corridors.

### Maps Folder

This folder contains multiple Python scripts designed to generate various map layouts for robotic path planning algorithms. The maps include general spaces, narrow paths, clustered obstacles, and maze-like structures.

- `Maps_file.py`: Includes map generation functions for general, narrow, cluster, and maze-like maps.
- `maze_map.py`: Focuses on generating a maze-like map with different types of obstacles.
- `plt_maps.py`: Visualizes the maps created by other scripts using `matplotlib`.

## Installation

To use this project, ensure you have the following Python packages installed:

```bash
pip install numpy matplotlib
```

## Usage

### Main Scripts

#### `ep_rrt_star_cluster.py`

This script generates a map with clustered square obstacles and attempts to find a path using the EP-RRT* algorithm.

**Parameters:**
- `width`: Width of the map.
- `height`: Height of the map.
- `num_squares`: Number of square obstacles.
- `square_size`: Size of each square obstacle.

**Usage:**
```bash
python ep_rrt_star_cluster.py
```

**Example Output:**
- A visual plot of the explored nodes and the optimal path found.

#### `ep_rrt_star_general.py`

This script generates a map with various geometric shapes, including rectangles, hexagons, and blocks, and attempts to find a path using the EP-RRT* algorithm.

**Parameters:**
- `width`: Width of the map.
- `height`: Height of the map.

**Usage:**
```bash
python ep_rrt_star_general.py
```

**Example Output:**
- A visual plot of the explored nodes and the optimal path found.

#### `ep_rrt_star_maze_map.py`

This script generates a maze-like map with rectangular and square obstacles and attempts to find a path using the EP-RRT* algorithm.

**Parameters:**
- `width`: Width of the map.
- `height`: Height of the map.

**Usage:**
```bash
python ep_rrt_star_maze_map.py
```

**Example Output:**
- A visual plot of the explored nodes and the optimal path found.

### Additional RRT* Scripts

Each script implements the RRT* algorithm in a specific environment:

#### `rrt_cluster.py`

Creates a random map with clustered square obstacles and attempts to find a path from a start position to a goal position.

**Usage:**
```bash
python rrt_cluster.py
```

#### `rrt_general.py`

Generates an obstacle map with predefined shapes like rectangles, hexagons, and walls, then finds a path from a start position to a goal position.

**Usage:**
```bash
python rrt_general.py
```

#### `rrt_maze.py`

Creates a complex maze-like obstacle map and finds a path from a start position to a goal position.

**Usage:**
```bash
python rrt_maze.py
```

#### `rrt_narrow.py`

Generates a narrow passage environment with tight spaces and corridors, and attempts to find a path from a start position to a goal position.

**Usage:**
```bash
python rrt_narrow.py
```

### Maps Folder

To generate and visualize the maps, run the `plt_maps.py` script:

```bash
python plt_maps.py
```

This will display the maps created by the various functions side by side in a single plot. The generated maps are represented in grayscale, where obstacles are denoted by higher intensity values.

**Map Functions:**
- `general_map(width, height)`: Creates a general map with predefined wall obstacles and rectangular shapes.
- `narrow_map(width, height)`: Generates a narrow map filled with multiple rectangular obstacles (fixed dimensions: 900x900).
- `cluster_map(width, height, num_squares, square_size)`: Constructs a map with random clusters of square obstacles.
- `maze_map(width, height)`: Creates a maze-like map with predefined obstacles and square obstacles scattered around the grid (fixed dimensions: 6000x3000).

## File Descriptions

### `ep_rrt_star_cluster.py`
- **Node Class**: Represents a point in the search space.
- **Functions**:
  - `plot_map`: Generates a map with square obstacles.
  - `check_collision`: Checks if a line segment collides with obstacles.
  - `nearest`: Finds the nearest node in the tree to a given point.
  - `steer`: Steers the tree towards a given point.
  - `sample_ellipse`: Samples points within an ellipse for informed sampling.
  - `plot_tree`: Plots the tree of explored nodes.
  - `backtrack_path`: Backtracks from the goal node to find the path.
  - `rrt_star_informed`: Main function implementing the EP-RRT* algorithm.

### `ep_rrt_star_general.py`
- **Node Class**: Represents a point in the search space.
- **Functions**:
  - `plot_map`: Generates a map with various geometric obstacles.
  - `check_collision`: Checks if a line segment collides with obstacles.
  - `nearest`: Finds the nearest node in the tree to a given point.
  - `steer`: Steers the tree towards a given point.
  - `sample_ellipse`: Samples points within an ellipse for informed sampling.
  - `plot_tree`: Plots the tree of explored nodes.
  - `backtrack_path`: Backtracks from the goal node to find the path.
  - `rrt_star_informed`: Main function implementing the EP-RRT* algorithm.

### `ep_rrt_star_maze_map.py`
- **Node Class**: Represents a point in the search space.
- **Functions**:
  - `plot_map`: Generates a maze-like map with rectangular and square obstacles.
  - `check_collision`: Checks if a line segment collides with obstacles.
  - `nearest`: Finds the nearest node in the tree to a given point.
  - `steer`: Steers the tree towards a given point.
  - `sample_ellipse`: Samples points within an ellipse for informed sampling.
  - `plot_tree`: Plots the tree of explored nodes.
  - `backtrack_path`: Backtracks from the goal node to find the path.
  - `rrt_star_informed`: Main function implementing the EP-RRT* algorithm.

### `rrt_cluster.py`
- **Node Class**: Represents a node in the RRT tree with properties such as position (`point`), parent node (`parent`), and cost to reach the node.
- **Functions**:
  - `plot_map`: Generates a map with randomly placed square obstacles.
  - `check_collision`: Checks if a line segment collides with obstacles.
  - `nearest`: Finds the nearest node to a given point from the list of nodes.
  - `steer`: Steers from a given node towards a target point with a specified step size.
  - `plot_tree`: Visualizes the RRT tree on the map.
  - `backtrack_path`: Backtracks from the goal node to the start node to find the complete path.

### `rrt_general.py`, `rrt_maze.py`, `rrt_narrow.py`
- Same structure as `rrt_cluster.py`, but with environment-specific map generation and handling.

## RRT* Algorithm (`rrt_star`)

The `rrt_star` function in these scripts implements the RRT* algorithm with the following steps:
1. **Initialization**: Creates the initial node (start position).
2. **Sampling**: Samples random points in the space.
3. **Nearest Node**: Finds the nearest node to the sampled point.
4. **Steering**: Creates a new node towards the sampled point.
5. **Collision Check**: Checks for collision-free paths.
6. **Adding Nodes**: Adds the new node to the tree if collision-free.
7. **Goal Check**: Checks if the goal is reached.
8. **Path Optimization**: Optimizes the path by minimizing the cost.

## License

This project is licensed under the MIT License.

 See the [LICENSE](LICENSE) file for details.

---
