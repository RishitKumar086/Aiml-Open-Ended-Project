# Autonomous Car Simulation with NEAT

## Overview

This project implements a simulation environment where autonomous cars learn to navigate a complex map using neural networks evolved through the NEAT (NeuroEvolution of Augmenting Topologies) algorithm. The objective is to train these neural networks to drive the cars efficiently, avoiding obstacles represented on the map.

## Features

- **Simulation Environment**: Built using PyGame, the simulation provides a graphical interface where cars move within a defined map.
  
- **Neural Network Control**: Each car is equipped with a neural network that processes sensor data (radars) to make decisions such as turning left, turning right, accelerating, or decelerating.

- **Evolutionary Algorithm**: The NEAT algorithm evolves the neural networks over generations, adjusting their topology and connection weights to optimize performance based on a fitness function.

- **Map and Obstacles**: The map includes obstacles represented by specific colors (e.g., BORDER_COLOR) that cars must detect and avoid using their radars.

- **Visualization**: Real-time visualization of car movements, radar sensor outputs, and key simulation metrics like current generation and number of active cars.

## How to Run

1. **Install Dependencies**:
   - Ensure Python 3.x is installed.
   - Install required packages

2. **Setup Configuration**:
   - Adjust parameters in `config.txt` to customize NEAT settings such as mutation rates, population size, and neural network structure.

3. **Run the Simulation**:
   - Execute the main script (`python main.py`) to start the simulation.
   - The simulation window will display the evolving behavior of the cars and relevant statistics.

## Configuration

- **NEAT Configuration**: Modify settings in `config.txt` to fine-tune the evolutionary process, including activation functions, mutation rates, and population size.
