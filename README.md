# Traveling Salesperson Problem (TSP) Solver using Genetic Algorithm

This project implements a genetic algorithm to find an approximate solution to the Traveling Salesperson Problem (TSP). Given a set of cities, the algorithm finds the shortest possible route that visits each city exactly once and returns to the starting city.

## Overview

The Traveling Salesperson Problem (TSP) is a classic optimization problem. This implementation uses a genetic algorithm, a metaheuristic inspired by natural selection, to find a near-optimal solution.

## Features

-   **Random City Generation**: Generates random sets of cities for TSP instances.
-   **Distance Matrix**: Computes the pairwise distance matrix for efficient distance lookups.
-   **Genetic Algorithm**: Implements selection, crossover, and mutation operators.
-   **Elitism**: Preserves the best individuals across generations.
-   **Fitness Tracking**: Tracks and plots the best and average fitness over generations.
-   **Visualization**: Visualizes the TSP route and fitness progress.

## Implementation Details

### Constants

-   `POPULATION_SIZE`: Number of individuals in the population (default: 20).
-   `MUTATION_RATE`: Probability of mutation (default: 0.2).
-   `CROSSOVER_RATE`: Probability of crossover (default: 0.9).
-   `MAX_GENERATIONS`: Maximum number of generations (default: 500).
-   `ELITISM_COUNT`: Number of best individuals to keep (default: 2).
-   `NUM_CITIES`: Number of cities in the TSP instance (default: 15).

### Class: `TSPGeneticAlgorithm`

-   `__init__(self)`: Initializes the population, city coordinates, and distance matrix.
-   `compute_distance_matrix(self)`: Computes the distance matrix using Euclidean distance.
-   `initialize_population(self)`: Creates an initial population of random routes.
-   `calculate_fitness(self, individual)`: Calculates the fitness of a route (1 / total distance).
-   `evaluate_population(self)`: Evaluates the population and tracks best and average fitness.
-   `selection(self)`: Selects parents using roulette wheel selection.
-   `crossover(self, parent1, parent2)`: Performs partially mapped crossover (PMX).
-   `mutation(self, individual)`: Applies swap mutation.
-   `create_new_generation(self)`: Creates a new generation using genetic operators and elitism.
-   `run(self)`: Runs the genetic algorithm.
-   `plot_results(self)`: Plots the fitness progress.
-   `visualize_solution(self, solution)`: Visualizes the best TSP route.



## Output

After running the script, you will see:

-   The best route found by the genetic algorithm.
-   The fitness of the best route (1 / distance).
-   A plot showing the fitness progress over generations.
-   A visualization of the TSP route.

