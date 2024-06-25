# Reinforcement Learning Environment

This Python script simulates a reinforcement learning environment where an agent navigates a grid-based puzzle, making decisions based on Q-learning principles to maximize rewards. The script includes functionality for representing the environment, defining possible actions, and running learning episodes to update the Q-values.

## Features

- **Environment Representation**: Represents a grid-based environment where each cell can be free space (' '), an obstacle ('#'), a positive reward ('+'), or a negative reward ('-').
- **Action Definition**: Defines the possible actions (UP, RIGHT, DOWN, LEFT) that the agent can take.
- **State Management**: Manages the state of the agent including its position and the current environment.
- **Q-Learning**: Implements a Q-learning algorithm where the agent learns to navigate the environment by choosing actions that maximize future rewards.

## Classes and Methods

- **`Action`**: Represents an action with its name and movement offsets (dx, dy).
- **`State`**: Represents the current state of the agent in the environment, handles action execution, and checks for the legality of actions.
- **`Env`**: Represents the environment, handles state initialization, and provides methods for accessing and modifying the environment.
- **`QTable`**: Manages a table of Q-values for state-action pairs, updates Q-values based on the agent's experience, and can print the Q-values for all actions.

## Learning Algorithms

- **`learn_episode()`**: Runs a single learning episode. The agent starts at a random state and makes decisions until it reaches an end state. The Q-values are updated based on the rewards received and the future potential rewards.
- **`learn()`**: Runs multiple episodes of learning, adjusting Q-values progressively to improve the agent's decision-making strategy.

## Usage

To use the script, run it with the desired command and arguments from the command line:

```bash
python environment_simulator.py learn <environment_string>
