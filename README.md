# Snake-Game-Deep-Q-RL

## Problem Statement

Using reinforcement learning, create a Snake game-playing agent that will aim to score by consuming food pellets while staying out of collisions. Explore novel methods for autonomous gameplay by utilizing neural network architectures and RL techniques, contributing to AI research in gaming settings.

## Introduction

A project based on reinforcement learning (RL) is focused on creating a Snake game-playing agent. We define the game environment, establish actions, and create a Q-network architecture that facilitates the agent's decisions. The agent's performance can be improved through the use of Deep Q-Learning, experience replay, and training. We aim to balance exploration and exploitation while striving for optimal gameplay. We aim to develop an autonomous agent that can maximize scores without causing collisions by utilizing evaluation and parameter tuning. The endeavor highlights RL's aptitude for handling intricate gaming situations and supports advancements in AI research related to autonomous gameplay.

## Contributors

- Swaraj Gambhir
- Anmol Khetan

## Approach

This method employs Deep Q-Learning to train an AI agent for autonomous Snake game play. Actions include up, down, left, or right movements in the grid-based environment. Q-values, approximated by a neural network, guide actions. Experience replay buffers past experiences for efficient training. An epsilon-greedy strategy balances exploration and exploitation. Performance evaluation ensures adept navigation, measuring average score and gameplay, with adjustments for optimal results.

- Environment Definition: Establishes the game on a grid, where actions involve movements: up, down, left, or right.
- Q-Network: Utilizes a neural network to approximate Q-values, representing expected rewards for actions in specific states.
- Experience Replay: Stores past experiences in a buffer for efficient training, enhancing learning stability.
- Training with Deep Q-Learning: Iteratively updates the Q-network to minimize temporal difference loss, aligning predicted rewards with actual outcomes.
- Exploration vs. Exploitation: Implements an epsilon-greedy strategy to balance exploration (trying new actions) and exploitation (choosing actions with highest Q-values).
- Performance Evaluation: Assesses the agent's performance through measuring average score and observing gameplay, enabling adjustments for optimal results.

## Design Details

1. **Environment**:
The Snake game environment consists of a grid with boundaries, snake body segments, food pellets, and potential collision hazards.

2. **States**:
States represent the current configuration of the game board, including the positions of the snake segments, food, and potential collision hazards such as walls or itself.

3. **Actions**:
Actions encompass movements the snake can take: up, down, left, or right. These actions are discrete choices defining the snake's direction.

4. **Reward**:
The reward system provides feedback to the agent. Positive rewards are given for consuming food pellets, negative for colliding with walls or itself. A large reward is assigned for completing the game by achieving a specific score.

5. **Agent Definition (Mathematical Formulation)**:
The agent is represented as a Deep Q-Network (DQN), utilizing neural networks. It accepts game states as input and outputs Q-values for each possible action. The agent's policy is to select actions greedily based on these Q-values, incorporating exploration via an epsilon-greedy strategy.

6. **Deep Q-Network (DQN)**:
DQN is chosen for its efficient approximation of the Q-function, enabling effective learning in complex environments like Snake.

7. **Replay Memory**:
Replay memory stores past experiences, facilitating learning from diverse transitions and reducing correlation between updates.

8. **Epsilon-Greedy Strategy**:
Balancing exploration and exploitation, epsilon-greedy strategy ensures a gradual shift from exploration to exploitation as the agent learns about the Snake game environment.

9. **Neural Network Representation**:
Neural networks approximate the Q-function, capturing game dynamics for informed decision-making based on current states.

10. **Training Process**:
The agent undergoes training using supervised learning and reinforcement learning techniques, enhancing its policy through repeated interactions and reward feedback from the Snake game environment.

## Work Done and Results

1. **Implementation of DQN for Snake Game**:
  - Initialization of the DQN model with appropriate input, hidden, and output sizes.
  - Definition of the neural network architecture using PyTorch modules.
  - Implementation of the training method for computing target Q-values and minimizing the squared error loss.

2. **Training Process**:
  - Conditional training start to accumulate sufficient experiences in the replay memory.
  - Sampling of experiences from the replay memory for decorrelation and training stability.
  - Batch processing and preprocessing of the sampled experiences.
  - Forward pass and backpropagation for updating the neural network weights.
  - Epsilon decay for managing the exploration-exploitation balance.

3. **Agent's Progress**:
  - Initial tests show the agent's ability to navigate the Snake game environment, avoid obstacles, and collect rewards.
  - Visual representations of the agent's gameplay and training progress over time.

4. **Performance Metrics**:
  - Game execution loop for iterating through a specified number of games.
  - Recording game data for later analysis.
  - Performance evaluation metrics, including average score, scores per game, win rate, and game outcome records.

5. **Challenges Faced**:
  - Complexity of environment representation and modeling.
  - Agent exploration and exploitation balance.
  - Action space management for discrete actions.
  - Memory management and efficient replay memory usage.
  - Hyperparameter tuning for optimal learning dynamics.
  - Computational complexity and resource constraints.

## Conclusion

The project successfully implements a Deep Q-Learning agent for autonomous gameplay in the Snake game environment. The agent demonstrates promising results in navigating the game, avoiding collisions, and maximizing scores. While challenges were encountered, such as environment complexity, exploration-exploitation balance, and computational constraints, the project contributes to AI research in gaming settings by exploring novel methods for autonomous gameplay using neural network architectures and reinforcement learning techniques.
