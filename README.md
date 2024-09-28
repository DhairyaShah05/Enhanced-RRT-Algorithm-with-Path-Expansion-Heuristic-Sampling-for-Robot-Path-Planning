```markdown
# Enhanced-RRT-Algorithm-with-Path-Expansion-Heuristic-Sampling-for-Robot-Path-Planning

## Project Structure

- `ep_rrt_star_cluster.py`: Implements the EP-RRT algorithm for a clustered map with square obstacles.
- `ep_rrt_star_general.py`: Implements the EP-RRT algorithm for a general map with different geometric shapes as obstacles.
- `ep_rrt_star_maze_map.py`: Implements the EP-RRT algorithm for a maze-like environment with rectangular and square obstacles.

## Installation

To use this project, ensure you have the following Python packages installed:

```bash
pip install numpy matplotlib
```

## Usage

### `ep_rrt_star_cluster.py`

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

### `ep_rrt_star_general.py`

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

### `ep_rrt_star_maze_map.py`

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

## Future Work

The following functionalities will be added in the future:
- [ ] Adding more complex maps in the `Maps` folder.
- [ ] Implementing different RRT variants in the `RRT` and `RRT-Connect` folders.
- [ ] Enhancing the visualization and performance of the algorithms.

## References

- Lavalle, Steven M. "Rapidly-Exploring Random Trees: A New Tool for Path Planning." (1998).
- Karaman, Sertac, and Emilio Frazzoli. "Sampling-based algorithms for optimal motion planning." The international journal of robotics research 30.7 (2011): 846-894.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

```
