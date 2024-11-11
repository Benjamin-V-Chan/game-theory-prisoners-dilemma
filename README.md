# Game Theory: Prisoner's Dilemma Simulation

Welcome to the **game-theory-prisoners-dilemma** simulation project! This project simulates the famous game theory experiment, the Prisoner's Dilemma, by testing various algorithms against each other in repeated rounds. The simulation aims to analyze which strategies perform best over time in this classic dilemma, giving insight into cooperative versus competitive behavior.

## Overview

The **Prisoner's Dilemma** is a well-known game theory problem involving two individuals (or algorithms, in this case) who can choose to either cooperate with or betray the other. If both cooperate, they each receive a moderate reward. If one betrays while the other cooperates, the betrayer gains a large reward while the cooperator gets nothing. If both betray, both receive a smaller penalty. The challenge lies in balancing self-interest with the potential benefits of cooperation over repeated interactions.

In this simulation, we pit multiple algorithms against each other over a series of rounds to determine which strategies yield the highest total reward. The outcomes of these interactions can provide insights into optimal strategies under different conditions.

## Project Structure

- **Simulation**: Each algorithm competes against every other algorithm (including itself) in a set number of rounds. At the end of the simulation, the total scores for each algorithm are compiled to reveal the best-performing strategies.

- **Configuration**: A `config.json` file allows you to customize various settings of the simulation, including:
  - Number of rounds per match
  - List of algorithms to test
  - Scoring system (e.g., points for cooperate-cooperate, cooperate-betray, etc.)
  - Matches against each algorithm
  
- **Analysis**: After the simulation, a script analyzes the results and provides visualizations of algorithm performance. This analysis highlights the strategies that tend to yield the highest rewards and explores how different configurations affect outcomes.

## Files

- **`simulator.py`**: The main script that runs the simulation. It loads configuration settings, runs matches between algorithms, and stores the results.
- **`config.json`**: The configuration file for adjusting simulation settings, including the algorithms tested, the number of rounds per match, and scoring rules.
- **`analyze_results.py`**: A script that processes the simulation data, visualizes results, and provides insights into the most successful strategies.
- **`algorithms/`**: A folder where all different algorithm files are stored and taken from for when the simulator needs them to run the matches.
- **`results/`**: A folder where output files (e.g., CSV files with results from each simulation run) are saved for easy access and further analysis.

## Algorithms

A set of predefined algorithms is included in the simulation, each implementing a different strategy (e.g., always cooperate, always defect, tit-for-tat, random). These strategies interact over multiple rounds, showcasing their effectiveness against various opponents.

You can also add your own algorithms by defining their logic in the appropriate module and adding them to the configuration.

## Getting Started

1. Clone this repository:
   ```bash
   git clone https://github.com/Benjamin-V-Chan/game-theory-prisoners-dilemma.git
   cd game-theory-prisoners-dilemma
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Modify the `config.json` file to adjust the simulation settings as desired.

4. Run the simulation:
   ```bash
   python simulator.py
   ```

5. Analyze the results:
   ```bash
   python analyze_results.py
   ```

## Analyzing & Visualizing Results

The `analyze_results.py` script analyzes the data into comprehensive statistics as well as generates visualizations showing the performance of each strategy across all matches
