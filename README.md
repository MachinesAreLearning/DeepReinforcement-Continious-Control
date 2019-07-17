# DeepReinforcement-Continious-Control
# Udacity-Deep Reinforcement learning(DRL)-Continuous-Control


![environment](https://github.com/rrishi2/DeepReinforcement-Continious-Control/blob/master/images/environement.gif)


## Introduction
This repository contains a Deep Deterministic Policy Gradients (DDPG) agent running in the Unity ML Agent.In this environment, a double-jointed arm can move to target locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal of your agent is to maintain its position at the target location for as many time steps as possible.
The observation space consists of 33 variables corresponding to the position, rotation, velocity, and angular velocities of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.

The DDPG is implemented in Python 3 using PyTorch.

The full report can be found here. (https://github.com/rrishi2/DeepReinforcement-Continious-Control/blob/master/report.pdf)

Code log is placed here.(https://github.com/rrishi2/DeepReinforcement-Continious-Control/blob/master/Continuous_Control_Code_Run.pdf)


### The Environment
For this project, we will provide you with two separate versions of the Unity environment:

    The first version contains a single agent.
    The second version is a 3D environment contains 20 double joined arms agents who can move freely to reach the target locations.

The second version is useful for algorithms like PPO, A3C, and D4PG that use multiple (non-interacting, parallel) copies of the same agent to distribute the task of gathering experience. 



### Goal
Note that your project submission need only solve one of the two versions of the environment.
Option 1: Solve the First Version

The task is episodic, and to solve the environment, your agent must get an average score of +30 over 100 consecutive episodes.
Option 2: Solve the Second Version

The goal is to control the 20 arms to move to their individual target locations and keep them there as many time steps as possible.

The barrier to solving the second version of the environment is slightly different, to take into account the presence of many agents. In particular, your agents must get an average score of +30 (over 100 consecutive episodes, and overall agents). Specifically,

    After each episode, we add up the rewards that each agent received (without discounting), to get a score for each agent. This yields 20 (potentially different) scores. We then take the average of these 20 scores.
    This yields an average score for each episode (where the average is over all 20 agents).

As an example, consider the plot below, where we have plotted the average score (overall 20 agents) obtained with each episode

![Result](https://github.com/rrishi2/DeepReinforcement-Continious-Control/blob/master/images/Result.JPG)


The environment is considered solved when the average (over 100 episodes) of those average scores is at least +30. 

## Environment Solved Criteria:
The environment is considered solved when the average mean score of all agents reach 30+ in the last 100 epsisodes.


### Unity Environment
Unity Machine Learning Agents (ML-Agents) is an open-source Unity plugin that enables games and simulations to serve as environments for training intelligent agents.

For game developers, these trained agents can be used for multiple purposes, including controlling NPC behavior (in a variety of settings such as multi-agent and adversarial), automated testing of the game builds and evaluating different game design decisions pre-release.

In this course, you will use Unity's rich environments to design, train, and evaluate your own deep reinforcement learning algorithms. You can read more about ML-Agents by perusing the [GitHub repository](https://github.com/Unity-Technologies/ml-agents).


### Requeriments:
- tensorflow: 1.7.1
- Pillow: 4.2.1
- matplotlib
- numpy: 1.11.0
- pytest: 3.2.2
- docopt
- pyyaml
- protobuf: 3.5.2
- grpcio: 1.11.0
- torch: 0.4.1
- pandas
- scipy
- ipykernel
- jupyter: 5.6.0

### Running the code

After you install the unity agent following these [instructions] (https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Readme.md), start your jupyter notebook and open the Continuous_Control.ipynb solution notebook and execute each cell.

### Getting Started
1. Install Unity ML
https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Installation.md

2. Download the Unity ML environment from one of the links below based on your OS:
    - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux.zip)
    - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher.app.zip)
    - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86.zip)
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86_64.zip)

Then unzip the file and place the file in this project folder.

3. Create Conda Environment   

Install conda from conda.io. Create a new Conda environment with Python 3.6.

```bash
conda create --name deeprl python=3.6
source activate deeprl
```

4. Install Dependencies
```bash
cd python
pip install .
```


## How to run the agent
To start training, simply open *Continuous_Control.ipynb* in Jupyter Notebook and follow the instructions there:

Start Jupyter Notebook
```bash
jupyter notebook
```
Trained model weights is included for quickly running the agent and seeing the result in Unity ML Agent.
Simply skip the training step and run the last step of the *Continuous_Control.ipynb*

Install conda from conda.io. Create a new Conda environment with Python 3.6.

conda create --name deeprl python=3.6
source activate deeprl
Install Dependencies
cd python
pip install .

