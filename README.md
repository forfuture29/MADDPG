# MADDPG (Collaboration)


The goal of this project is to solve the Tennis Environment with the tasks as follows:

Goal : Two agents control rackets to bounce a ball over a net as long as possible

State Sizes  : 24 (8 observation spaces with three consecutives frame)

Action Sizes : 2

Number of Agents: 2

Reward:  If an agent hits the ball over the net, +receives a reward of +0.1. If an agent lets a ball hit the ground or hits the ball out of bounds, it receives a reward of -0.01.

Enviroment Solved:  An average score of +0.5 (over 100 consecutive episodes, after taking the maximum over both agents)


# Getting Start

1. First, we have to set up the environment by following the instructions in the [DRLND GitHub repository](https://github.com/udacity/deep-reinforcement-learning#dependencies)
2. Download the Unity Environment using the link as below:


<br />Linux: [Click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux.zip)
<br />Mac OSX: [Click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis.app.zip)
<br />Windows (32-bit): [Click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86.zip)
<br />Windows (64-bit): [Click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86_64.zip)

Then, place the file in the p3_collab-compet/ folder in the DRLND GitHub repository, and unzip the file.


(For Windows users) Check out [this link](https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64) if you need help with determining if your computer is running a 32-bit version or 64-bit version of the Windows operating system.


(For AWS) If you'd like to train the agent on AWS (and have not [enabled a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md), then please use [this link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Linux_NoVis.zip) (version 1) or [this link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux_NoVis.zip) (version 2) to obtain the "headless" version of the environment. You will not be able to watch the agent without enabling a virtual screen, but you will be able to train the agent. (To watch the agent, you should follow the instructions to [enable a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md), and then download the environment for the Linux operating system above.)


# How to run the code

You can run the code from both Nagivation.ipynb and Report.ipynb. I recommend to run the code in Report.ipynb. The instructions have been divided into many steps which all you have to do is to follow each step consecutively. Please note that you need to import the environment by changing the `file_name` parameter to match the location of the Unity environment that you downloaded.


# More on how to start the virtual environment on your local computer

To give an example of how i create the virtual environment on my local computer, i will illustrate more on the steps and problems that i encounter.

1. First, i start by cloning the repository:
`git clone https://github.com/udacity/deep-reinforcement-learning.git`

2. Next, i create the virtual environment (my operating system is windows): 

```
conda create --name drlnd python=3.6
conda activate drlnd
```

3. Third step is to install torch using whl file since the torch 0.4.0 in dependency is a bit too old to use pip.
   The whl file can be downloaded from [here](https://download.pytorch.org/whl/torch_stable.html)
   
4. Now, we can install all the necessary libraries and create IPython kernel for the `drlnd` environment.

```
cd deep-reinforcement-learning/python
pip install .
pip install gym
python -m ipykernel install --user --name drlnd --display-name "drlnd"
```

5. Once, every step is completed, we can download the Unity environment.  Place the file in the p3_collab-compet/ folder and start running.

