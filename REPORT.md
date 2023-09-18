[//]: # (Image References)

[image1]: https://raw.githubusercontent.com/fredericosantos/DRLN_ContinuousControl/master/Graph.png "Scores"

# Report on Project 2: Continuous Control

## Learning Algorithm

### Learning Algorithm

I used the DDPG algorithm for this project. I used the recently released Rectified Adam as my optimizer.

### Hyperparameters

The hyperparameters values I selected were:

BUFFER_SIZE = int(1e6)  # replay buffer size
BATCH_SIZE = 128        # minibatch size
GAMMA = 0.99            # discount factor
TAU = 1e-3              # for soft update of target parameters
LR_ACTOR = 0.001         # learning rate of the actor
LR_CRITIC = 0.001        # learning rate of the critic
WEIGHT_DECAY = 0        # L2 weight decay
LEARN_EVERY = 4        # learning timestep interval
LEARN_NUM = 1          # number of learning passes


### Model Architecture

Both Actor and Critic models are composed of 3 fully connected layers, with a 1D batch normalization layer from the first to second layer.

## Plot of Rewards

![Scores][image1]


## Ideas for Future Work

In the future I would like to be able to implement more advanced algorithms such as the D4PG that's more recent.

I would also like to work to implement Prioritized Experienced Replay so the Agent has a better replay pool.





