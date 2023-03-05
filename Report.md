# Description of the implementation

The goal of this project is to train DDPG algorithm to play Tennis in collaborative and cometetitve manners. In other words, solving multiple agents environment.

The core implementation is based on the previous project. The main modifications are as follows:

1. wrapping the ddpg_agent.Agent to MultiAgentDdpg classs so that it would be suitable for the problem.
2. chaning the noise function from uniform to gauss.
3. changing some the hyper parameters.

# Learning Algorithm

The report clearly describes the learning algorithm,

### hyperparameters

* BUFFER_SIZE = int(1e6)  # replay buffer size

* BATCH_SIZE = 256         # minibatch size

* GAMMA = 0.99            # discount factor

* TAU = 1e-3              # for soft update of target parameters

* LR_ACTOR = 1e-4         # learning rate of the actor 

* LR_CRITIC = 1e-4        # learning rate of the critic

* WEIGHT_DECAY = 0        # L2 weight decay

### Model architectures:

* Actor network's inputs are the state size and its output is the action size. There are 2 hidden layers each of which of size 256.

* Critic network:  It takes the states and action as input, its output is predicting a reward score. Two hiddent layers of size 256 are used.


# Plot of Rewards

The problem solved in 2048 episodes. The following figure shows the overall scores.
<img src="final_rl_score.png"  width="60%" height="30%">

# Ideas for Future Work
The submission has concrete future ideas for improving the agent's performance.
