# Autonomous Delivery Agent Project

This project implements an autonomous delivery agent navigating a 2D grid environment with static and dynamic obstacles, varying terrain costs, and multiple packages to deliver. The agent uses various search and planning algorithms to find optimal paths and demonstrates dynamic replanning in response to moving obstacles.

## Features

- **Grid Environment Modeling:** Supports static obstacles, dynamic obstacles (with time-varying positions), and terrain costs.
- **Pathfinding Algorithms:** Includes Breadth-First Search (BFS), Uniform Cost Search (UCS), A* Search, and Hill Climbing with Random Restarts.
- **Autonomous Delivery Agent:** Plans and executes package deliveries, logs results, supports dynamic replanning in changing environments.
- **Test Map Generation:** Provides small, medium, large, and dynamic environments for experimentation.
- **Experimental Framework:** Compares algorithms on all maps and provides performance analysis and visualization.
- **Demonstrations:** Animates agent movement and replanning under dynamic conditions.
- **Command Line Interface (CLI):** Interactive CLI for running planners and experiments.

## Requirements

- Python 3.6+
- [NumPy](https://numpy.org/)
- [matplotlib](https://matplotlib.org/)
- [IPython](https://ipython.org/) (for display/animation in notebooks)

Install dependencies via pip:
```sh
pip install numpy matplotlib ipython
```

## File Structure

- All code is contained in a single `.py` file (see provided code).
- No external data files required; all maps and scenarios are generated programmatically.

## How It Works

### Environment

The `GridEnvironment` class models the grid, obstacles, terrain costs, packages, and agent position. It supports visualization using `matplotlib`.

### Search Algorithms

Supported algorithms:
- **BFS:** Finds the shortest path in terms of steps, ignores terrain cost.
- **UCS:** Finds the least-cost path considering terrain.
- **A\* Search:** Uses Manhattan distance as heuristic; optimal and efficient.
- **Hill Climbing:** Fast local search with random restarts, suitable for dynamic replanning.

All algorithms inherit from a base class `SearchAlgorithm`.

### Delivery Agent

The `DeliveryAgent` class plans and executes deliveries, adapts to dynamic obstacles, and logs details of the run. It supports replanning mid-delivery if obstacles change.

### Experiments & Analysis

- `run_experiments()`: Runs all algorithms on all maps and stores results.
- `analyze_results()`: Plots cost, computation time, success rates, and provides a summary table.
- Demonstrations visualize agent behavior in the presence of moving obstacles.

### CLI

A command-line interface (`run_planner_cli()`) lets users:
- Select map and algorithm to run.
- Compare all algorithms on a map.
- Run comprehensive experiments.
- View dynamic replanning demonstrations.

## Usage

### 1. Run Full Demonstration

```sh
python autonomous_delivery_agent.py
```
Follow the on-screen prompts to choose between automated demonstration or CLI mode.

### 2. Run via CLI

Start the CLI and interactively select maps/algorithms:
```sh
python autonomous_delivery_agent.py
```
Choose "Interactive CLI mode" when prompted.

### 3. In Jupyter Notebook

Import the classes and run demonstrations visually:
```python
from autonomous_delivery_agent import *
main()
```

## Example Outputs

- Visualizations of the environment, agent paths, and obstacles.
- Bar charts comparing algorithm performance.
- Animated demonstrations of dynamic replanning.

## Customization

- **Maps:** Modify `create_test_maps()` to define new environments.
- **Algorithms:** Extend `SearchAlgorithm` to add new planning methods.
- **Agent Behavior:** Customize `DeliveryAgent` for more complex tasks or replanning policies.

## Project Structure

- `GridEnvironment`: Environment simulation, visualization.
- `SearchAlgorithm`, `BFS`, `UCS`, `AStarSearch`, `HillClimbingSearch`: Pathfinding.
- `DeliveryAgent`: Delivery logic, logging, replanning.
- Experiments and analysis functions.
- CLI for interactive usage.



**Enjoy exploring autonomous path planning and delivery agent simulation!**
