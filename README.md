# Navigation

In this project, an agent navigates in a square world full of yellow and blue bananas. The agent receives a reward of +1 when collecting a yellow banana, and a reward of -1 for collecting a blue banana. Our goal is to train the agent to navigate and collect as many yellow bananas as possible. The task is episodic and the environment is considered to be solved when the agent gets an average score of +13 over 100 consecutive episodes. The environment has a state space of 37 dimensions. Those correspond to data such as the agent's velocity and ray-based meaurements of the surrounding. The agent has a set of four available actions:

* 0: forward
* 1: backward
* 2: left
* 3: right
