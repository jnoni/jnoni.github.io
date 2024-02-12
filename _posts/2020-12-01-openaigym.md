---
layout: post
title: A comparative study of Reinforcement Learning techniques
subtitle: Done over multiple OpenAI Gym environments
bigimg: /img/path.jpg
tags: [Reinforcement Learning, Q learning, Pacman, Deep Q Network]
---

TL;DR
Implemented a set of RL based algorithms on different virtual environments. Primary aim: To reason out why one algorithm works better than the other on a particular environment.

## Abstract
OpenAI Gym is a toolkit used for a purpose of developing and comparing reinforcement learning algorithms. It has a collection of environments that we can use to work out our reinforcement learning algorithms. In our project, we worked on Pacman and Frozen Lake environments. Pacman agent has an objective to maximize its award points by eating the big fruits, while keeping itself safe from the ghost. Frozen Lake agent has an objective to reach the goal state while being alive. If it steps into a hole, it gets a -1 reward and dies. Classical AI agents require you to have intact knowledge of the rules and the states of the game. In this project, we implement Q-Learning approach on these two environments. This doesnt require us to have a complete knowledge of the states and rules beforehand, the algorithm learns it. We also implemented the Deep Reinforcement Learning (DQN) approach and drew comparisons from the results obtained from the two.

## Background

As a part of his PhD thesis, Watkins, J.C.H. [1] (1989) namely, Learning from Delayed Rewards, introduced a simple and intuitive approach for agents to learn by mistake for how to act optimally in controlled Markovian environment. It makes extensive use of the Dynamic Programming paradigm which works by successively improving the evaluations of the quality of particular actions at particular states. The Q-Learning approach introduced by them could learn the optimal control directly without the need to model the transition probabilities or expected rewards of the MDP. 

DeepMind technologies, in their 2013 paper on Deep Rein- forcement Learning [2], introduce the concept of approximat- ing the Q-Value function for large state space environments. In this approach, they used Convolutional Neural Networks with fully connected layers. Their input is raw pixels and output is a value function which helps in determining the future rewards. They applied their method on seven Atari games from the Arcade Learning environment. In the paper [3] performs a comparison study on the performance of different activation functions for convolutional neural network. It concluded that Exponential Linear Units (ELUs) performs best in comparison to other activation functions. They argues that ELUs speeds up the learning process in the Deep Neural Networks and leads to higher classification accuracy. In our project, we have incorporated these techniques in our project to observe how they perform on Pacman and Frozen Lake environments by tuning three hyper parameters namely, decay of exploration rate, learning rate, and discount factor. And, we present our analysis and draw conclusions from the plots obtained.

## Algorithms

In Reinforcement Learning algorithms, we try to match an input to an action to maximize the rewards or profit. System is not fed with hard-coded values to determine which actions to take, rather it follows the methodology of Trial and error and learns the best actions itself. It tries to take future performance into context in an attempt to perform better, because this approach is designed in a way that its present actions affect its future rewards.

- Q learning
- Q table
- Deep Q Networks

## Conclusion

- We conclude that due to large space requirements of Q learning algorithms, they are not feasible for complicated problem statements with large number of states.
- Deep Q Networks show good performance in a large search spaces.
- Deep Q learning requires good amount of training before it can perform nicely enough.

Detailed Report and Results: https://drive.google.com/file/d/1KkbN8mDrvb4p-FKLreIxkwTmCQzP3Tqr/view?usp=sharing
