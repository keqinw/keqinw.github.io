---
permalink: /
title: "Projects"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---


[MAN: Multi-Agent Networks Learning](http://keqinw.github.io/MAN)
-----
We introduce a novel Deep Reinforcement Learning (DRL) algorithm called Multi-Agent Networks (MAN) Learning, to especially solve the discrete action space problems. We manually separate the action space into two smaller parts, and create one Value Neural network for each of them. Then MAN uses temporal-difference learning to train these networks synchronously, which is easier than training one networks with large action output directly. We first test MAN on a block stacking problem where we come up the basic idea of MAN, and then extend MAN for tackling 12 games with 18 action spaces of the Atari Arcade Learning environment.  
![](https://github.com/keqinw/keqinw.github.io/raw/master/images/pipeline.png "pipeline of MAN")  

[A DRL Framework Towards Drawing Single-stroked Handwriting Image](http://keqinw.github.io/draw)
-----
We came up with an innovative end-to-end framework that combines the CNN and PPO to control the manipulator to draw single-stroked pictures on a flat surface. In perticular, we preprocessed the raw 2D image from UNIPEN dataset and extracted features with CNN; and we applied model-free method PPO in inverse kinematics solving that enable the manipulator to reach the destination, utilizing Hindsight Experience Replay (HER) and Goal Condition (GC) technique to accelerate the training. To evaluate the performance of our framework, we tested the framework in the real world to draw simple letters and shapes on ROS platforms.  
<iframe
    width="640"
    height="480"
    src="https://www.youtube.com/embed/ylg1y9e7aGo"
    frameborder="0"
    allow="autoplay; encrypted-media"
    allowfullscreen
>
</iframe>

[Parallel Robot System for Objects Sorting](http://keqinw.github.io/parallel)
----
We designed a new parallel structure of robotic arm that can move faster than normal arms, inspired by the structure of Delta 3D printer and set up the mechanical and electrical structures. In experiment, we applied the Parallel Robot System in a real-world assembly line, in which the robotic arm detects the position of the randomly placed objects and stacks them separately by color and type.

[Late but Safe: Control Car Braking with Delay-Aware Reinforcement Learning](http://keqinw.github.io/late)
------
We solved an action-delay problem with a model-based algorithm Delay-Aware Trajectory Sampling (DATS). We trained a probabilistic ensembled model as the transition function, which could predict the distribution of current cart state given the previous state and the future actions; utilized Cross-Entropy Method to search the next action, given the prediction from ensembled network.  
Left: brake with PPO, the cart cannot exactly stop at the point bue to the action-delay. Right: brake with DATS, the cart could overcome the action-delay.  
<!-- ![](https://github.com/keqinw/keqinw.github.io/raw/master/images/brake_delay.gif | width=100) -->
<img src="https://github.com/keqinw/keqinw.github.io/raw/master/images/brake_delay.gif" width="300" height="300">
<img src="https://github.com/keqinw/keqinw.github.io/raw/master/images/brake-delay-MBRL-DATS.gif" width="300" height="300">
 
