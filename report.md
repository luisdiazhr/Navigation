# Report

This is the report


## Learning Algorithm 

In this project, the DQN algorithm is used to solve the environment. This algorithm uses a neural network to map the state to a action-value function. 


* Initialize replay memory D with capacity N
* Initialize weights of the DQN agent
* Since we have a fixed Q target network, weights are just copied from the primary network

### Architecture

The DQN algorithm uses two separate neural networks with identical architectures. The architecture is implemented by the `QNetwork` class located in `model.py`. The model includes an input layer, a couple of hidden layers with 64 units each, followed by a fully connected layer. The dimension of the input layer is the same as the state dimension and the size of the output layer corresponds to the action size space. The output is a value for each possible action given the current state.

Without this, there would be harmful correlations. The target network weights are updated less often than the primary network. The implementation of the DQN Agent is contained in `dqn_agent.py`. 

### Replay Memory

As the agent starts interacting with the environment, the experiences are stored in a replay memory. Then, a random batch is extracted from this memory and the neural network learns from it by using gradient descent. The act of extracting a random batch is called experience replay. This randomness breaks correlation among experiences and allows the agent to learn from the same experiences multiple times. 

It is important to say that learning cannot take place until there is a good amount of experiences in the replay memory. 
 
## Future improvements
