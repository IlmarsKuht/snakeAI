# SnakeAI: Deep Reinforcement Learning in Action

## Overview
SnakeAI is a deep learning project where an AI algorithm learns to play the game of Snake. The projectuses Deep Q Learning and Long Short-Term Memory (LSTM) to create a self-learning AI capable of navigating complex scenarios and improving its performance over time.

## Game Mechanics
The AI is trained to play Snake, a game where the primary objective is to grow the snake by consuming apples while avoiding collisions with the snake's body or the game boundaries. The AI receives environmental input in the form of a state vector:

`[danger left, danger right, danger straight, direction left, direction right, direction up, direction down, food left, food up, food right, food down]`

Each element of this state vector is a boolean representing the immediate environment of the snake.

For example, the state `[0, 0, 0, 0, 0, 1, 0, 1, 0, 0, 0]` indicates no immediate danger, with the snake moving upwards and the food located left.

## Neural Network Architecture
The SnakeAI employs a multi-layer linear neural network model built using PyTorch. The network includes:

- **Long Short-Term Memory (LSTM) Layers**: Enhances the AI's ability to remember and leverage past actions and outcomes, vital for strategic decision-making in complex environments.
- **Linear Hidden Layers**: Processes the input state to determine the best course of action, with outputs corresponding to move left, move right, or move straight.

## Reinforcement Learning
The AI leverages Reinforcement Learning (RL) principles, where it learns optimal gameplay strategies through trial and error. This learning process is characterized by:

- **Reward System**: Gaining +10 reward for eating an apple and receiving -10 as a penalty for running into the wall or itself.
- **Exploration Strategy**: For the initial 80 games, the AI focuses on exploration to understand various aspects of the game environment.

## Performance Visualization
The training progress and performance of the AI are visually represented in a graph, where:
- **Blue Lines**: Indicate the score of each game.
- **Orange Line**: Represents the moving average of the scores, showcasing the learning progression of the AI.

![snake](https://user-images.githubusercontent.com/115834230/199955735-cd24b08f-9020-40da-bc98-528de06ad1c4.png)
