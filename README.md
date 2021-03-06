# Simulated Annealing for Travelling Salesman Problem

This repository describes the solution for the travelling salesman problem using simulated annealing.

Given the list of cities in Russia, it is needed to solve the travelling salesman problem for the 30 most populated cities. That is, we need to find the shortest path connecting all 30 cities.

[sa_salesman.ipynb](https://github.com/noteisenheim/travelling_salesman/blob/master/sa_salesman.ipynb) notebook contains the solution code and a brief report.

Brief description of the algorithm is the following:

1. Generate a random path connecting the cities, select initial temperature `T` and annealing rate `anneal_rate`
2. Generate next candidate path: select two cities at random, reverse the path between them
3. With the probability of  ๐=๐^((๐๐๐_๐๐๐กโ_๐๐๐๐๐กโโ๐๐๐ค_๐๐๐กโ_๐๐๐๐๐กโ)/๐)  accept the new path as the new state, otherwise leave the old path
4. Update  ๐=๐โ(1โ๐๐๐๐๐๐_๐๐๐ก๐)
5. Continue with steps 2-4 until the temperature does not fall down close to 0
6. The resulting state is supposed to be close to the shortest path possible

Here you can see the visualization of the process for finding the shortest route conencting the cities.

![Visualization](https://raw.githubusercontent.com/noteisenheim/travelling_salesman/master/visualization.gif)
