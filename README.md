# DRLND-Navigation-Project
The github submission of the first project of Udacity's nanodegree program entitled "Navigation"

## Requirements

To set up your python environment to run the code in this repository, follow the instructions below.

1. Create (and activate) a new environment with Python 3.6.

    - __Linux__ or __Mac__:

    ```bash
    conda create --name drlnd python=3.6
    source activate drlnd
    ```

    - __Windows__:

    ```bash
    conda create --name drlnd python=3.6 
    activate drlnd
    ```

2. Clone the repository (if you haven't already!), and navigate to the `python/` folder.  Then, install several dependencies.

    ```bash
    cd python
    pip install .
    ```

3. On Anaconda

    ```bash
    conda install pytorch=1.7.0 -c pytorch
    ```

4. Then create an [IPython kernel](http://ipython.readthedocs.io/en/stable/install/kernel_install.html) for the `drlnd` environment.

    ```bash
    python -m ipykernel install --user --name drlnd --display-name "drlnd"
    ```

## DQN with experience replay

![Image 1](banana.gif?style=centerme)

The goal of this project is to train an agent to collect yellow bananas and avoid blue bananas in an Unity environment.

### States

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around the agent's forward direction. Given this information, the agent has to learn how to best select actions.

### Actions

Four discrete actions are available, corresponding to:

`0` : move forward

`1` : move backward

`2` : turn left

`3` : turn right

### Reward

A reward of **+1** is provided for collecting a yellow banana, and a reward of **-1** is provided for collecting a blue banana. Thus, the goal of your agent is to collect as many yellow bananas as possible while avoiding blue bananas.

The task is episodic, and in order to solve the environment, your agent must get an average score of +13 over 100 consecutive episodes.

### DQN Model Specifications

The deep RL model used to train the agent is a Deep-Q-Network with experience replay.

The Q-network is a fully connected ANN consisting of 2 hidden layers with 128 nodes each.

The model parameters can be found in dqn_agent.py and the associated jupyter notebook.

### Results
