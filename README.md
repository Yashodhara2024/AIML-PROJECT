# Autonomous Delivery Agent

This project implements an autonomous delivery agent that navigates a 2D grid city to deliver packages using various pathfinding algorithms.

## Features

- Grid environment with static obstacles and varying terrain costs
- Support for dynamic moving obstacles
- Three pathfinding algorithms:
  - Uninformed Search (BFS/Uniform-cost)
  - Informed Search (A* with admissible heuristic)
  - Local Search (Hill-climbing with random restarts)
- Experimental comparison of algorithms
- Dynamic replanning capability

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/autonomous-delivery-agent.git
cd autonomous-delivery-agent

HOW TO EXECUTE THE PROJECT -->
numpy==1.24.3
matplotlib==3.7.1
