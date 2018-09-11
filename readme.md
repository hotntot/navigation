# Banana Navigation meets Deep Q-Network (DQN)

### Project details

This is an implementation of a DQN agent being trained to collect yellow bananas and avoid blue ones.

There are 4 possible actions and a state space that looks like:
[1.         0.         0.         0.         0.84408134 0.
 0.         1.         0.         0.0748472  0.         1.
 0.         0.         0.25755    1.         0.         0.
 0.         0.74177343 0.         1.         0.         0.
 0.25854847 0.         0.         1.         0.         0.09355672
 0.         1.         0.         0.         0.31969345 0.
 0.        ]
States have length: 37

After you are able to get the code working, try to change the parameters in the notebook, to see if you can get the agent to train faster!  You may also like to implement prioritized experience replay, or use it as a starting point to implement a Double DQN or Dueling DQN!

### Dependencies

The agent was trained using
 * Python=3.6
 * Cuda 9.2 - with a corresponding GPU unit (https://developer.nvidia.com/cuda-zone)
 * Unity Environment (https://store.unity.com/)
 * Any additional packages are detailed in the environment.yml fil


### Instructions

Run the navigation.ipynb notebook to train the agent.

### Results

The environment is considered solved when the average score >= 13 over 100 episodes. The agent achieved an average score of 14.0 after 486 training episodes.