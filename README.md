# Reinforcement Learning Projects Summary
Projects for Deep Reinforcement Learning in Unity environment: 

* [Navigation trained with DQN:](https://github.com/yueureka/ReinforcementLearning/tree/master/Navigation_DQN) 
In this project, DQN algorithm is used train the Banana agent. The agent has a state space of 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around the agent's forward direction. Four discrete actions are available, corresponding to a reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana. The task is episodic, after trained with DQN algorthm for 700 esposides, we reached an average score of 14.26 for 100 episode.

<p align="center">
  <img width="460" height="300" src="https://github.com/yueureka/ReinforcementLearning/blob/master/Navigation_DQN/Pics/banana.gif">
</p>


* [Researcher trained with DDPG:](https://github.com/yueureka/ReinforcementLearning/tree/master/Continuous-Control)
In this project, DDPG algorithm is used to train the Researcher agent. We've 20 identical agents in the enviroment, each agent has an observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints.

<p align="center">
  <img width="460" height="300" src="https://github.com/yueureka/ReinforcementLearning/blob/master/Continuous-Control/Pics/reacher.gif">
</p>
  
* [Multi-Agent task: Tennis trained by DDPG:](https://github.com/yueureka/ReinforcementLearning/tree/master/Continuous-Control)
This project is similar to Researcher projects, but with two independet agents playing with each other. In this environment, two agents control rackets to bounce a ball over a net. If an agent hits the ball over the net, it receives a reward of +0.1. If an agent lets a ball hit the ground or hits the ball out of bounds, it receives a reward of -0.01. Thus, the goal of each agent is to keep the ball in play.
The observation space consists of 8 variables corresponding to the position and velocity of the ball and racket. Each agent receives its own, local observation with a total of 24 states. Two continuous actions are available, corresponding to movement toward (or away from) the net, and jumping.

<p align="center">
  <img width="460" height="300" src="https://github.com/yueureka/ReinforcementLearning/blob/master/MultiAgent_Tennis/pictures/Tennis.gif">
</p>
