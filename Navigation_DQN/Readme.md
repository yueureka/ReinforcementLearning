# Introduction

In this project, we are going to use DQN algorithm from Deep Reinforcement Learning to train an Unity agent to navitate in a large, squared world. In the envrioment, a reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana. Thus, the goal of your agent is to collect as many yellow bananas as possible while avoiding blue bananas.

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around the agent's forward direction. Four discrete actions are available, corresponding to:

0 - move forward.

1 - move backward.

2 - turn left.

3 - turn right.

The task is episodic, after trained with DQN algorthm for 700 esposides, we reached an average score of 15.09 for 100 episode.

## File Description 
 * Navigation.ipynb -- the notebook that load and train the Navigation agent, it also describes the theory of DQN and the code to train the agent.
 * dqn_agent.py -- the python library that contains the Agent class and RelayBuffer class, it will be imported to the Navigation.ipynb to train the agent. 
 * model.py -- the torch class for DQN model
 * checkpoint_2000iterations.pth -- the saved model that's been trained with DQN algorithm, you may direct load the model and run the agent.  

## Installation Instruction

The code runs in Python 3.6, Python libraries such as numpy, random, collections and matplotlib are used in the code. Tensorflow 1.7.1 and Pytorch 0.4.0 is used to train the model, and GPU mode is applied during the training process.

If you want to run the code on your own computer, here's the instruction on how to set up the Unity Environment:

* Step 1: Clone the DRLND Repository
If you haven't already, please follow the instructions in the [DRLND GitHub](https://github.com/udacity/deep-reinforcement-learning#dependencies) repository to set up your Python environment. These instructions can be found in README.md at the root of the repository. By following these instructions, you will install PyTorch, the ML-Agents toolkit, and a few more Python packages required to complete the project.
(For Windows users) The ML-Agents toolkit supports Windows 10. While it might be possible to run the ML-Agents toolkit using other versions of Windows, it has not been tested on other versions. Furthermore, the ML-Agents toolkit has not been tested on a Windows VM such as Bootcamp or Parallels.

* Step 2: Download the Unity Environment. 
Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip)
Then, place the file in the p1_navigation/ folder in the DRLND GitHub repository, and unzip (or decompress) the file.
(For AWS) If you'd like to train the agent on AWS (and have not enabled a virtual screen), then please use this link to obtain the "headless" version of the environment. You will not be able to watch the agent without enabling a virtual screen, but you will be able to train the agent. (To watch the agent, you should follow the instructions to enable a virtual screen, and then download the environment for the Linux operating system above.)

* Step 3: Explore the Environment. 
After you have followed the instructions above, open Navigation.ipynb (located in the p1_navigation/ folder in the DRLND GitHub repository) and follow the instructions to learn how to use the Python API to control the agent.
