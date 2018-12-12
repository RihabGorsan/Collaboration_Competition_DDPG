# Collaboration and Competition project: p3 in DRLND 
---
## Project details: 

This project is being done as part of the Udacity Deep Reinforcement Learning Nanodegree, a four month course that I am taking. In this project, two agents control rackets to bounce a ball over a net.

## Environment details: 

The environment is episodic and involves playing with two agents.</br>
If an agent hits the ball over the net, it receives a reward of +0.1. If an agent lets a ball hit the ground or hits the ball out of bounds, it receives a reward of -0.01. Thus, the goal of each agent is to keep the ball in play.
</br>
The observation space consists of 8 variables corresponding to the position and velocity of the ball and racket. Each agent receives its own, local observation. Two continuous actions are available, corresponding to movement toward (or away from) the net, and jumping.
</br>
The task is episodic, and in order to solve the environment, your agents must get an average score of +0.5 (over 100 consecutive episodes, after taking the maximum over both agents). Specifically,
</br>
After each episode, we add up the rewards that each agent received (without discounting), to get a score for each agent. This yields 2 (potentially different) scores. We then take the maximum of these 2 scores.
This yields a single score for each episode.</br>
The environment is considered solved, when the average (over 100 episodes) of those scores is at least +0.5.

## Getting started

1. Clone this repo using `git clone https://github.com/RihabGorsan/Collabboration_Competition_DDPG.git` </br>
2. Begin by importing the necessary packages. So first create a conda environment  </br>
`conda create --name navigation python=3.6` </br>
and then install the following packages: </br>
`conda install -y pytorch -c pytorch` </br>
`pip install unityagents==0.4.0 ` </br>
`pip install mlagents` </br>

3. Download the Banana unity environment 
You can download the environment form one  of the links below. Just please select the enviornment that matches your OS

    - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux.zip)
    - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis.app.zip)
    - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86.zip)
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86_64.zip)

Unzip the file hen place it in the cloned project. 


## Train your agent
You can execute each code block in the ddpg notebook to train the agent using DDPG.  This will fire up the Unity environment and output live training statistics to the command line.  When training is finished you'll have the two saved models in `checkpoint_actor.pth` and  `checkpoint_critic.pth`.

Feel free to experiment with modifying the hyperparameters to see how it affects training:

- [model.py](model.py) : you can change the architecture of the network.
- [ddpy_agent.py](ddpg_agent.py) : play with the hyperparams of the RL agent.

## Report
See the [report](report.md) for more details.  
