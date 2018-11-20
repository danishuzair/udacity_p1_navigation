# Project 1: Navigation: README file

### 1. Introduction

The objective of the project is to train an agent in the "Banana" environment, where an agent navigates an environments which has yellow and blue bananas. The agent has to collect bananas, and collecting a yellow banana results in a reward of +1, and collection a blue banana results in a reward of -1. The goal of the agent is to maximize the reward. The environment is considered "solved" if the agent collects an average reward of 13 over 100 consecutive episodes.

Within the environment, the agent can be in a state space which has a dimension of 37. The state space contains the agents velocity, along with a ray-based perception of objects in the agent's forward direction.

The agent has four actions available to it, which are the following:
- 0 - move forward
- 1 - move backward
- 2 - turn left
- 3 - turn right

The agent has to select the best action to take in its current state, factoring in the reward structure of +1 for yellow bananas collected and -1 for blue bananas collected.

### 2. Installing dependencies
To able to run the training environment, the following dependencies need to be installed:
Setup your environment per the instructions found in the README file in the following [link](https://github.com/udacity/deep-reinforcement-learning#dependencies)

Download the Unity environment from the link below that matches your operating system:
- Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip)
- Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana.app.zip)
- Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86.zip)
- Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip)

### 3. Running the scripts
The main file that will take care of initializing the environment, doing the training, and running a trained agent in the environment is the Navigation.ipynb file. Before running this file, ensure that the following files are at the same location as the Navigation.ipynb file:
- dqn_agent.py
- model.py
- Banana.app
- checkpoint.pth (or checkpoint13score.pth or checkpoint17score.pth or checkpoint2000iterations.pth)

### 4. Importing all the libraries
To import all the required libraries, run the block of code in the first section of the Navigation.ipynb script. This section is titled "Importing Libraries".

### 5. Taking random actions in the environment
To have an agent take random actions in the environment, follow the steps below:
1. Restart the jupyter notebook kernel
2. Run the code in section 1 of Navigation.ipynb: "Importing Libraries"
3. Run the code in section 2 of Navigation.ipynb: "Opening the environment and taking random actions"

### 6. Training an agent using Deep Q-Learning
To train an agent using Deep Q-Learning, follow the steps below:
1. Restart the jupyter notebook kernel
2. Run the code in section 1 of Navigation.ipynb: "Importing Libraries"
3. Run the code in section 3 of Navigation.ipynb: "Training an agent"

### 7. Run a trained agent in the environment
To run a trained agent in the environment, follow the steps below:
1. Restart the jupyter notebook kernel
2. Run the code in section 1 of Navigation.ipynb: "Importing Libraries"
3. Ensure you are pointing to the correct "checkpoint" in section 4 of Navigation.ipynb: "Run environment using a trained agent (by importing a checkpoint)"
4. Run the code in section 4 of Navigation.ipynb: "Run environment using a trained agent (by importing a checkpoint)"

### 8. Available checkpoints
As part of the github project, a few checkpoints have been provided that can be used to run a trained agent in the environment. The details of the checkpoints are as follows:
- "checkpoint.pth" and "checkpoint13score.pth" are essentially the same. In both cases, the checkpoints were saved as soon as an average score of greater than 13 was obtained over 100 consecutive episodes, and the training was stopped.
- "checkpoint17score.pth" is a checkpoint when an average score of greater than 17 was obtained over 100 consecutive episodes.
- "checkpoint2000iterations.pth" is a checkpoint when the training was allowed to continue for a complete 2000 iterations, and there was no early-stopping based on a certain score criteria being met.
