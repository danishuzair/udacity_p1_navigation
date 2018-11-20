# Project 1: Navigation: Report

### 1. Introduction

For the first project of the Udacity Deep Reinforcement Class, the goal was to use Deep Q-Learning to train an agent to navigate a Banana world. In this world, there were four main entities, the agent, empty space, locations with yellow bananas, and locations with blue bananas. The agent navigated its way around the environment, and if it collected a yellow banana it received a reward of +1, and if it collected a blue banana, it received a reward of -1. The agent had four actions available to it, which were move forward, move backward, turn left, or turn right. The agent also received information abouts its current state, which consisted of the agents velocity along with a ray-based perception of objects in the agent's forward direction. By considering its current state, the agent had to decide to take one of the four available actions, and the goal of the agent is to maximize its reward.

### 2. Deep Q-Learning
Deep Q-Learning is a class of algorithms in which the optimal action value function q* is in the form of a neural network. This is unlike traditional Q-Learning, in which the optimal action value function q* is in the form of a table.

One of the major issues that is presented when a neural network is used as the optimal action value function is that the learning becomes unstable. Deep Q-Learning provides a solution to this issue by using the following two techniques:
1. Experience replay
2. Fixed Q-targets

In the case of experience replay, the agent generates an experience pool, and randomly samples from it to use for the learning. As the agent learns, the experience pool gets updated, and the agent continues randomly sampling from it.

In the case of fixed Q-targets, a slightly older version of the Q-network is used to compute the losses. This target network is kept separate from the learned network, and whereas the learned network is updated after every iteration, the target network is updated more slowly. This slower update of the target network helps stabilize the learning process.

### 3. Neural network architecture and hyperparameters
The input to the neural network was the current state of the agent, which had a dimension of 37. The neural network had 3 layers, which each layer being fully connected. The details of the layers are as follows:
- Layer 1: Fully connected - 37 dimension input, 64 dimension output, Relu activation function
- Layer 2: Fully connected - 64 dimension input, 64 dimension output, Relu activation function
- Layer 3: Fully connected - 64 dimension input, 4 dimension output

For the output layer, an element-wise mean squared error loss was used to make the updated to the weights of the network.

Apart from this, the hyperparameters that were used were as follows:
- Buffer size: 10,000
- Batch size: 64
- Discouting factor: 0.99
- Learning rate: 5e-4
- Update every: 4
- Maximum number of episodes: 2000
- Epsilon start: 1
- Epsilon end: 0.01
- Epsilon decay: 0.995

### 4. Results
A few different training sessions were run to train the agent. Initially, the goal was to stop training and consider the environment "solved" once the agent got an average reward of 13 over 100 consecutive episodes. Using the hyperparameters listed in the previous section, the agent was able to solve the environment in 405 episodes. The table below provides the results of this learning.
![Results](Output.png)