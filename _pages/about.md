---
permalink: /
title: "Projects"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---


MAN: Multi-Agent Networks Learning
-----
We introduce a novel Deep Reinforcement Learning (DRL) algorithm called Multi-Agent Networks (MAN) Learning, to especially solve the discrete action space problems. We manually separate the action space into two smaller parts, and create one Value Neural network for each of them. Then MAN uses temporal-difference learning to train these networks synchronously, which is easier than training one networks with large action output directly. We first test MAN on a block stacking problem where we come up the basic idea of MAN, and then extend MAN for tackling 12 games with 18 action spaces of the Atari Arcade Learning environment.  
![](https://github.com/keqinw/keqinw.github.io/raw/master/images/pipeline.png "pipeline of MAN")  

A DRL Framework Towards Drawing Single-stroked Handwriting Image
-----
We came up with an innovative end-to-end framework that combines the CNN and PPO to control the manipulator to draw single-stroked pictures on a flat surface. In perticular, we preprocessed the raw 2D image from UNIPEN dataset and extracted features with CNN; and we applied model-free method PPO in inverse kinematics solving that enable the manipulator to reach the destination, utilizing Hindsight Experience Replay (HER) and Goal Condition (GC) technique to accelerate the training. To evaluate the performance of our framework, we tested the framework in the real world to draw simple letters and shapes on ROS platforms.  
[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/ylg1y9e7aGo/0.jpg)](https://www.youtube.com/watch?v=ylg1y9e7aGo)
