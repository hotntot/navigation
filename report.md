# DQN implementation

This project implements a vanilla DQN model as first described by DeepMind (https://storage.googleapis.com/deepmind-media/dqn/DQNNaturePaper.pdf)

Critical components:
 * Local Q-network
 * Target Q-network
 * Replay memory of (S, A, R, S') tuples
 * Epsilon greedy actions

### Neural Network model

The two Q-networks are identical in structure:
 * inputs - state_size (37)
 * first linear layer (64)
 * relu activation
 * second linear layer (64)
 * relu activation
 * output layer - action size (4)

 * Loss & training: MSE with Adam optimizer

### Hyperparameters
 * Decaying epsilon from 1.0 to 0.01 with decay 0.995 every episode
 * learning rate 5e-4
 * batch size 64
 * replay memory size 1e5
 * tau 1e-3 for soft updating target parameters
 * updating every 4 steps

### Results achieved

![image1]: (./average_score_per_episode.png) "Average score per episode"

### Ideas for future work

There are several ways of improving vanilla DQNs like:
 * Double DQN (DDQN)
 * Prioritized experience replay
 * Dueling DQN
 * Learning from multi-step bootstrap targets
 * Distributional DQN
 * Noisy DQN

All of these ideas have been shown to perform better than vanilla DQN. But the best results would probably be achieved by combining them all in an algorithm called Rainbow (https://arxiv.org/abs/1710.02298).

Since the criterion was met with vanilla DQN (13.0 point avg over 100 episodes) it should be expected to be achieved faster with any/all of the above methods.