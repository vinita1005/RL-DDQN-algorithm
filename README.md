# RL-DDQN-algorithm

# Agent trained on 100+ episodes:
![caption](https://github.com/vinita1005/RL-DDQN-algorithm/blob/main/openaigym.video.28.episode8.video001000_Trim.gif)

The agent managed to score between 50-200

# Agent trained on 1000+ episodes:

![caption](https://github.com/vinita1005/RL-DDQN-algorithm/blob/main/openaigym.video.28.episode8.video001000_Trim%20(3).gif)

The agent managed to score between 1800 - 3000

It was observed that the dqn algorithm often overestimates the q-value for certain actions.
For example, if there are 2 actions. One of them yeilds a higher immediate reward but
the other one leads to an optimal policy. In this case, the DQN will have higher q-values
for the 1st action. This prevents the agent from learning the optimal policy effectively.
To overcome this problem, DeepMind propsed the double dqn algorithm. In this algorithm,
instead of taking max of q-values while computing the target q-values for training,
the primary network will first choose an action for that state and the target network will
compute the target q-value for that state and action.

So, there will be 2 estimators:

Q1 - To obtain best actions

Q2 - To evaluate Q for the above action

Compared to DQN, finding a perfect balance of all the hyper parameters to attain maximum
rewards is much more difficult in DDQN.
