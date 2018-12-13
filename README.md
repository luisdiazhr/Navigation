# Project: Navigation

### Introduction
In this project, an agent navigates in a square world full of yellow and blue bananas. 

![alt text](agent.gif "Agent")

The agent receives a reward of +1 when collecting a yellow banana, and a reward of -1 for collecting a blue banana. Our goal is to train the agent to navigate and collect as many yellow bananas as possible. The task is episodic and the environment has a state space of 37 dimensions. Those correspond to data such as the agent's velocity and ray-based meaurements of the surrounding. The agent has a set of four available actions:

* 0: forward
* 1: backward
* 2: left
* 3: right

The goal of this project is to get the agent gets an average score of +13 over 100 consecutive episodes.

### Installation

1. Download the environment from one of the links below. You need only select the environment that matches your operating system:

* Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip)
* Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana.app.zip)
* Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86.zip)
* Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip)

Download the file into the top level directory of this repo and unzip it.

### Getting started

Follow the instructions in `Navigation.ipynb` to get started.
