# Navigation
Submission of first project in Deep Reinforcement Learning Nanodegree Program in Udacity
The goal of the project is to teach an agent to navigate in a large square world, while collecting as many bananas as possible. This is reinforcement learning task, in which agent starts in some state, makes an action (based on its policy), and environment responds to agent by change of state and returning a reward. This reward signals to agent whether its action is good or bad. So, as some people say, reinforcement learning is “scientific” representation of trial-and-error.
This “banana” environment is provided by The Unity Machine Learning Agents Toolkit (ML-Agents). This Unity plugin, which Machine Learning Agents (ML-Agents) is an open-source Unity plugin that enables games and simulations to serve as environments for training intelligent agents. In other words, Unity gives a chance for machine learning scientists to train their algorithms and visualize how the trained agent is performing through animations (which is really cool and fun!). 
Going back to our “banana” environment:
State space: 37. It includes agent's velocity, along with ray-based perception of objects around the agent's forward direction.
Action space: 4, discrete:
•	0 - move forward.
•	1 - move backward.
•	2 - turn left.
•	3 - turn right.

Reward space: 2. A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana. 
Thus, the goal of our agent is to collect as many yellow bananas as possible while avoiding blue bananas. Given this information, the agent has to learn how to best select actions.

The task is episodic, and in order to solve the environment, the agent must get an average score of +13 over 100 consecutive episodes.

The problem was solved with vanilla DQN algorithm with 2 hidden layers in episodes.
The code was written in python v3, using pytorch. GPU is not extremely necessary, as network is not so deep and state-space is not too large.

How to run:
There are 4 files required to run the project. 
•	Navigation.ipynb is a Jupiter notebook with main code and the only file that need to be run.
If you would like to use GPU,  then you will need to firstly go through parts 1, 2, 4 and train your agent, then disable GPU and run parts (if your variables are lost) 1, 2, 3, 5 and see how your agent performs.
•	dqn_agent.py is a python script which contains our reinforcement learning algorithm with replay buffer and fixed targets of Q function. 
•	Model.py is a python script which contains our deep neural network
•	checkpoint.pth is our file with saved model weights.
Note: The Unity ML-Agent team frequently releases updated versions of their environment. We are using the v0.4 interface. To avoid any confusion, please use the workspace we provide here or work with v0.4 locally.

Useful links:
You can study DQN paper (https://www.cs.toronto.edu/~vmnih/docs/dqn.pdf)
More about Unity agents (https://github.com/Unity-Technologies/ml-agents)
More about Udacity Deep Reinforcement Learning (https://udacity.com)
If you got really excited about RL, then you can read book written by “father” of Reinforcement Learning (http://incompleteideas.net/book/the-book-2nd.html)
