# Introduction

In this project, we are going to use DDPG algorithm from Deep Reinforcement Learning to train the muti agent task from Unity [Tennis](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#tennis).

![Unity agent-Researcher](https://github.com/yueureka/ReinforcementLearning/blob/master/Continuous-Control/Pics/reacher.gif)

In this environment, two agents control rackets to bounce a ball over a net. If an agent hits the ball over the net, it receives a reward of +0.1. If an agent lets a ball hit the ground or hits the ball out of bounds, it receives a reward of -0.01. Thus, the goal of each agent is to keep the ball in play.

The observation space consists of 8 variables corresponding to the position and velocity of the ball and racket. Each agent receives its own, local observation. Two continuous actions are available, corresponding to movement toward (or away from) the net, and jumping.

The task is episodic,after solving the environment, the agents achieve an average score of +0.75 (over 100 consecutive episodes, after taking the maximum over both agents).

After each episode, we add up the rewards that each agent received (without discounting), to get a score for each agent. This yields 2 (potentially different) scores. We then take the maximum of these 2 scores.
This yields a single score for each episode.
The environment is considered solved, when the average (over 100 episodes) of those scores is at least +0.5.

The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.

We've 20 identical agents in the enviroment, the task is episodic with 1000 total time steps per episode, after trained with DDPG algorthm for 176 esposides, we reached an average score of 36.96 for 100 episodes.

![Scores during training](https://github.com/yueureka/ReinforcementLearning/blob/master/Continuous-Control/Pics/TrainingScore.PNG)
![Scores of 100 episodes](https://github.com/yueureka/ReinforcementLearning/blob/master/Continuous-Control/Pics/TestScore.PNG)

## File Description 
 * Countinuous_control.ipynb -- the notebook that load and train the Navigation agent, it also describes the theory of DDPG and the code to train the agent.
 * DDPG_agent.py -- the python library that contains the Agent class, RelayBuffer and OUNoise class, it will be imported to the Navigation.ipynb to train the agent. 
 * model.py -- the torch class for both Actor and Critic class of the DDPG model
 * checkpoint_actor.pth.pth -- the saved actor torch model that's been trained with DQN algorithm, you may direct load the model and run the agent.  
 * checkpoint_critic.pth.pth -- the saved critic torch model that's been trained with DQN algorithm, you may direct load the model and run the agent.  

## Installation Instruction

The code runs in Python 3.6, Python libraries such as numpy, random, collections and matplotlib are used in the code. Tensorflow 1.7.1 and Pytorch 0.4.0 is used to train the model, and GPU mode is applied during the training process. The total training time is around 10 hours. 

If you want to run the code on your own computer, here's the instruction on how to set up the Unity Environment:

* Step 1: Clone the DRLND Repository
If you haven't already, please follow the instructions in the [DRLND GitHub](https://github.com/udacity/deep-reinforcement-learning#dependencies) repository to set up your Python environment. These instructions can be found in README.md at the root of the repository. By following these instructions, you will install PyTorch, the ML-Agents toolkit, and a few more Python packages required to complete the project.
(For Windows users) The ML-Agents toolkit supports Windows 10. While it might be possible to run the ML-Agents toolkit using other versions of Windows, it has not been tested on other versions. Furthermore, the ML-Agents toolkit has not been tested on a Windows VM such as Bootcamp or Parallels.

* Step 2: Download the Unity Environment. 
Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86_64.zip)
Then, place the file in the p1_navigation/ folder in the DRLND GitHub repository, and unzip (or decompress) the file.
(For AWS) If you'd like to train the agent on AWS (and have not enabled a virtual screen), then please use this link to obtain the "headless" version of the environment. You will not be able to watch the agent without enabling a virtual screen, but you will be able to train the agent. (To watch the agent, you should follow the instructions to enable a virtual screen, and then download the environment for the Linux operating system above.)

* Step 3: Explore the Environment. 
After you have followed the instructions above, open Countinuous_control.ipynb and follow the instructions to learn how to use the Python API to control the agent.
