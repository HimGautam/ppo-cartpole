# ppo-cartpole

This project is based on Proximal Policy Optimization (PPO) algorithm. Link to the paper can be found [here](https://arxiv.org/pdf/1707.06347.pdf).

![ezgif com-gif-maker (1)](https://user-images.githubusercontent.com/70597091/163183497-f072a9df-c82c-42d9-a94e-54cf7267ee94.gif)

# Overview

This project solves the control problem in CartPole balancing by using PPO algorithm. The PPO algorithm belongs to class of algorithms known as Policy Gradients which directly optimizes the policy objective. 

Input to the NN is an array of data containing following observations:
 ```Cart Position,	Cart Velocity, Pole Angle, Pole Velocity At Tip```
 
 Output of the NN are ```logits``` (unnormalized probability distributions). We construct Categorical Distribution using these logits and then actions are sampled from this distributions. Actions of this problem are:
 ```Push cart to the left or Push cart to the right```
 
 After training on 25000 steps of data, the Neural Network learns to balance the pole for some time. 
 
 Note: Different Activation Functions and Initializations yield different results. So far ```tanh``` Activation Function and Orthogonal Initialization yield best results.
 
 # Requirements
 
 This code requires following dependencies:
 
 1) Jupyter Notebook
 2) Python
 3) Open AI Gym
 4) Numpy
 5) Tensorflow
 6) Tensorflow-Probability
 7) Tensorboard

# Trying Out

Just run all cells and the NN will train in some time depending on the running speed of the machine. 
