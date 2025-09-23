Autonomous Delivery Agent: AI Pathfinding in a 2D Grid
This project implements an autonomous delivery agent that navigates a 2D grid city to deliver packages efficiently. The agent must model its environment, choose rational actions to maximize delivery efficiency, and handle dynamic obstacles by replanning its route.

#Features

Environment Modeling: The agent operates within a 2D grid environment that supports static obstacles, varying terrain costs, and dynamic moving obstacles.

Multiple Pathfinding Algorithms: The project includes implementations of:

Uninformed Search: Breadth-First Search (BFS) and Uniform-Cost Search (UCS).

Informed Search: A* with an admissible heuristic (Manhattan distance).

Local Search: Hill Climbing with Random Restarts, designed for dynamic replanning.

Dynamic Replanning: The agent is capable of replanning its path in real-time when it encounters unexpected obstacles or changes in the environment.

Experimental Analysis: The project includes a framework to compare the performance of each algorithm on different map instances, measuring metrics such as path cost, nodes expanded, and computation time.

Reproducibility: The code is structured to ensure test maps and results can be easily reproduced.


# How to Run the Project
Dependencies
This project requires the following Python libraries:

numpy
heapq
matplotlib
ipython

You can install them using pip:
pip install numpy matplotlib ipython
Running the Main Script
The project is designed to be run from the command line interface (CLI). The main() function in the main.py script orchestrates the entire process: creating maps, running experiments, analyzing results, and demonstrating dynamic replanning.

python main.py
This will:

Initialize and visualize four test maps: small, medium, large, and dynamic.

Run experiments, comparing the performance of BFS, UCS, A*, and Hill Climbing on each map.

Print and plot the experimental results.

Display a proof-of-concept animation or log showing the agent replanning its path on a dynamic map.

Code Structure

GridEnvironment: Models the 2D grid with terrain, static obstacles, and dynamic obstacles.

SearchAlgorithm: The base class for all pathfinding algorithms.

BFS: Implements Breadth-First Search.

UniformCostSearch: Implements Uniform-Cost Search.

AStarSearch: Implements A* with Manhattan distance heuristic.

HillClimbingSearch: Implements a local search strategy for replanning.

DeliveryAgent: The core agent class responsible for planning and executing deliveries.


create_test_maps(): Function to generate the required map instances.

run_experiments(): Function to execute the performance comparison tests.

analyze_results(): Function to generate plots and provide analysis of the experimental data.


demonstrate_dynamic_replanning(): Functions for the dynamic replanning proof-of-concept.


# Grid File Format
The grid environment can be represented by a simple text file. Each character or number in the file corresponds to a grid cell.


# or a high integer value (e.g., 9) can represent static obstacles.


1 or other low integer values represent terrain costs.

The start and goal positions can be denoted by specific characters (e.g., S for start and G for goal) or by coordinates specified in the main script.

Example of a small grid map file (small_map.txt):

1 1 1 1 1
1 # # 1 1
1 1 1 1 1
1 1 1 1 1
1 1 1 1 1
This project's create_test_maps() function generates the maps programmatically for convenience, but the underlying model supports this format.
