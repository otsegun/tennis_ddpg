[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/42135623-e770e354-7d12-11e8-998d-29fc74429ca2.gif "Trained Agent"
[image2]: https://user-images.githubusercontent.com/10624937/42386929-76f671f0-8106-11e8-9376-f17da2ae852e.png "Kernel"

# Continuous_Control for Reacher Agent

### Introduction

This project contains code for a trained reinforcement learning agent that solves the [Tennis](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#tennis) environment task of UnityML 

![Trained Agent][image1]

  
The environment consists of two agents controlling their rackets to bounce a ball over the net. A reward of +0.1 is given to an agent if it bounces the ball over the net. An agent gets a reward of -o.01 if it plays the ball out of bounds or allows it to hit the gound. Thus, the goal of the agent is to is keep the ball in play for as long as possible.

The state space is an array of 8 elements. It contains the position and velocity of the ball and the racket. Given this information, the agent has to learn how to best select actions. The action is an array of two elements corresponding to movement toward/away from the ball and jump. 

The task is episodic, and in order to solve the environment, **agents must get an average score of +0.5 (over 100 consecutive episodes, after taking the maximum over both agents)**. 


### Getting Started

#### Dependencies
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
2. Install Openai gym using `pip install gym`.
3. Install box2d and box2d-py: `pip install box2d`; `pip install box2d-py`. 
4. Clone the repository below and navigate to the `python/` folder.
```bash
git clone https://github.com/udacity/deep-reinforcement-learning.git
cd deep-reinforcement-learning/python
```
5. Replace the `requirements.txt` file in the `deep-reinforcement-learning/python` folder with the one provided in this repository. The difference is that pytorch has been bumped up to version 1.0.0. from version 0.4.0 in the original `deep-reinforcement-learning/python/requirements.txt` file. Then, install several dependencies with 

```bash
pip install .
```

6. Create an [IPython kernel](http://ipython.readthedocs.io/en/stable/install/kernel_install.html) for the `drlnd` environment. 

```bash
python -m ipykernel install --user --name drlnd --display-name "drlnd"
```

7. Before running code in a notebook, change the kernel to match the `drlnd` environment by using the drop-down `Kernel` menu. 

![Kernel][image2]

#### Setup Agent Environment

1. Download the environment from one of the links below.  You need only select the environment that matches your operating system:
    - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux.zip)
    - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis.app.zip)
    - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86.zip)
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86_64.zip)
        
        

2. Place the environment file in the `p3_collab-compet/` folder of the `deep-reinforcement-learning` folder that was cloned in the Dependencies section, and unzip (or decompress) the file.

3. Copy the `tennis_agent.py`, `actor_critic_model.py`, `checkpoint_actor.pth`, `checkpoint_critic.pth`, `Tennis.ipynb` files provided in this repository into the `p3_collab-compet/` folder of the `deep-reinforcement-learning` folder that was cloned in the Dependencies section. 

4. Start a jupyter notebook in the `drlnd` environment created in the Dependencies section. Set the kernel to `drlnd` kernel created in the Dependencies section.

#### Instructions

Follow the instructions in `Tennis.ipynb` to get started with training your own agent or watch an existing agent (provided  with the `checkpoint_actor.pth`, `checkpoint_critic.pth`) files perform the task!

