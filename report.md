# Report

This is the report


Learning Algorithm 

In this project, the DQN algorithm is used to solve the environment. This algorithm uses a deep neural network to represent the action-value function. The DQN takes the state as the input of the neural network

As the agent starts interacting with the environment, the experiences are stored in a replay memory. Then, a random batch is extracted from this memory and the neural network learns from it by using gradient descent. It is important to say that these steps are interleaved.

Initialize replay memory D with capacity N
Initialize weights of the DQN agent
Since we have a fixed Q target network, weights are just copied from the first network

It is important to say that learning cannot take place until there is a good amount of experiences in the replay memory. 
 
