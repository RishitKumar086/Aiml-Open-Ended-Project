# Autonomous Car Simulation with NEAT

## Overview

This project implements a simulation environment where autonomous cars learn to navigate a complex map using neural networks evolved through the NEAT (NeuroEvolution of Augmenting Topologies) algorithm. The objective is to train these neural networks to drive the cars efficiently, avoiding obstacles represented on the map.

## Features

- **Simulation Environment**: Built using PyGame, the simulation provides a graphical interface where cars move within a defined map.
  
- **Neural Network Control**: Each car is equipped with a neural network that processes sensor data (radars) to make decisions such as turning left, turning right, accelerating, or decelerating.

- **Evolutionary Algorithm**: The NEAT algorithm evolves the neural networks over generations, adjusting their topology and connection weights to optimize performance based on a fitness function.

- **Map and Obstacles**: The map includes obstacles represented by specific colors (e.g., BORDER_COLOR) that cars must detect and avoid using their radars.

- **Visualization**: Real-time visualization of car movements, radar sensor outputs, and key simulation metrics like current generation and number of active cars.

## Algorithm

 - **NEAT Algorithm:** NEAT evolves neural networks with varying topologies, adjusting both the weights and 
   the structure of the network. The algorithm involves selection, mutation, and crossover to generate new populations 
   of neural networks. Fitness evaluation is used to measure the performance of each neural network, guiding 
   the evolution process.

- **Collision Detection:** Each car checks for collisions by examining the color of the pixels at its corners.
   If any corner of the car sprite touches a white pixel, the car is considered crashed.
  
- **Sensor (Radar) Calculation:**
  Radars are simulated as lines extending from the car at different angles.
  Each radar measures the distance to the nearest border, which is used as input for the neural network.

- **Fitness Calculation:**
  The fitness of each car (and hence its neural network) is based on the distance traveled and the time it remains alive.
  This encourages neural networks to drive the car efficiently and avoid collisions for as long as possible.

## How to Run

1. **Install Dependencies**:
   - Ensure Python 3.x is installed.
   - Install required packages

2. **Setup Configuration**:
   - Adjust parameters in `config.txt` to customize NEAT settings such as mutation rates, population size, and neural network structure.

3. **Run the Simulation**:
   - Execute the main script (`python newcar.py`) to start the simulation.
   - The simulation window will display the evolving behavior of the cars and relevant statistics.

## Configuration

- **NEAT Configuration**: Modify settings in `config.txt` to fine-tune the evolutionary process, including activation functions, mutation rates, and population size.
