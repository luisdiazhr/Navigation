# Report

This is the report


## Deep Q-Network in Navigation 

In this project, the DQN algorithm is used to solve the environment. This algorithm uses a neural network to map the state to a action-value function. The 

* Initialize replay memory D with capacity N
* Initialize weights of the DQN agent
* Since we have a fixed Q target network, weights are just copied from the primary network

### 1. Architecture

The DQN algorithm uses two separate neural networks with identical architectures. The purpose of this is to The architecture is implemented by the `QNetwork` class located in `model.py`. The model includes an input layer, a couple of hidden layers with 64 units each, followed by a fully connected layer. The dimension of the input layer is 37 neurons, which is the same as the state dimension. The size of the output layer corresponds to the action size space which in this case is . The output is a value for each possible action given the current state. The implementation of the DQN Agent is contained in `dqn_agent.py`. 

### 2. Replay Memory

As the agent starts interacting with the environment, the experiences are stored in a replay memory. Then, a random batch is extracted from this memory and the neural network learns from it by using gradient descent. The act of extracting a random batch is called experience replay. This randomness breaks correlation among experiences and allows the agent to learn from the same experiences multiple times. It is important to say that learning cannot take place until there is a good amount of experiences in the replay memory. The following table shows the parameters used for the experience replay:

| Parameter       | Value         |
| ----------------|:-------------:| 
| Buffer size     | 1e5           | 
| Batch size      | 64            |  
| Learning rate   | 5e-4          |
| Discount factor | 0.99          |
| Update factor   | 4             |
| Soft update     | 1e-3          |
 
## Future improvements

Although the algorithm shows a good performance, some ideas of future work can be considered such as prioritizing the experiences. During the interaction, some experiences may be better than others. The problem is the algorithm samples randomly from the batch and there is no way to detect important experiences the agent could learn from. A good approach would be to assign priorities to the experiences based on the method TD error delta. The bigger the error, the more the agent has to learn from that experience. That error magnitude serves as a measurement of priority. One of the advantages of this method is that the agent learns faster since it requires less batch updates.
