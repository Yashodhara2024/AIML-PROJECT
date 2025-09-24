Autonomous Delivery Agent Project

This project implements an autonomous delivery agent that navigates a 2D grid environment. The agent's core task is to efficiently deliver packages by planning optimal paths while contending with varying terrain costs and dynamic obstacles. The project serves as a comprehensive case study in artificial intelligence, covering uninformed, informed, and local search algorithms.

Key Features 
Modular Environment Model: A GridEnvironment class that supports static obstacles, dynamic (moving) obstacles, and variable terrain costs.

Intelligent Agent Design: A DeliveryAgent class that plans and executes paths, demonstrating rational decision-making. It also includes a robust dynamic replanning mechanism.

Diverse Pathfinding Algorithms: The project provides implementations of several search algorithms for comparative analysis:

Uninformed Search: Breadth-First Search (BFS) and Uniform-Cost Search (UCS).

Informed Search: A* with an admissible Manhattan distance heuristic.

Local Search: Hill Climbing with Random Restarts, specifically for fast replanning.

Automated Experiments: A framework to run experiments on four distinct test maps (small, medium, large, and dynamic) and analyze algorithm performance based on path cost, time, and nodes expanded.

Proof-of-Concept: A built-in demonstration of dynamic replanning to show the agent's ability to adapt to sudden changes in the environment.

Setup Instructions
Follow these steps to set up and run the project.

1. Prerequisites
Make sure you have Python 3.6+ installed on your system. You will also need the following libraries:

numpy for handling numerical data and the grid map.

matplotlib for plotting and visualizing results.

ipython for the animation demonstration.

heapq (built-in) for priority queue implementations.

You can install the required libraries using pip:
pip install numpy matplotlib ipython

2. Running the Project
The project is designed to be run from the command line. Navigate to the project's directory and execute the main script:
python main.py

Running this command will:
Generate and visualize the four test maps.
Run automated experiments on all maps, comparing the performance of BFS, UCS, A*, and Hill Climbing.
Print detailed results for each algorithm and map combination.
Display a plot summarizing the experimental data.
Run a dynamic replanning demonstration to show the agent's reactive behavior.

3. Code Structure
The source code is modular and well-documented for easy understanding:

main.py: The entry point of the application, orchestrating all functions.

GridEnvironment: Defines the environment's properties and methods.

SearchAlgorithm: The base class for all search algorithms.

BFS, UniformCostSearch, AStarSearch, HillClimbingSearch: Implementations of each algorithm.

DeliveryAgent: Contains the agent's logic for planning and executing deliveries.

Helper functions (create_test_maps, run_experiments, analyze_results, etc.) are included to manage the automated testing and analysis framework.

Grid File Format
Although the test maps are programmatically generated for convenience and reproducibility, the underlying environment model supports a simple grid file format.

A grid map can be represented as a text file where each number or character corresponds to a cell's terrain cost or obstacle status. For example:

1 1 1 1 (low cost terrain)

2 2 1 1 (mixed terrain)


This format allows for the easy creation and sharing of new custom maps for additional testing.







