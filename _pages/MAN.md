---
title: "MAN: Multi-Agent Networks Learning"
permalink: /MAN/
author_profile: true
---
Learning within a large potential action space is pretty tricky in reinforcement learning, due to low exploration efficiency.  
We introduce a novel Deep Reinforcement Learning (DRL) algorithm called Multi-Agent Networks (MAN) Learn- ing, to especially solve the discrete action space problems. We manually separate the action space into two smaller parts, and create one Value Neural network for each of them. Then MAN uses temporal-difference learning to train these networks synchronously, which is easier than training one networks with large action output directly.  
![](https://github.com/keqinw/keqinw.github.io/raw/master/images/pipeline.png)


Above figure is the MAN structure schematic. The MAN firstly splits the original action into two sub-actions aI and aII; and then uses two streams to separately estimate values of sub-actions; finally combines these sub-actions back to the original action. Both networks output Q-values for each action. Viewing the content in the dashed box as a whole is the traditional reinforcement learning pipeline.  

![](https://github.com/keqinw/keqinw.github.io/raw/master/images/loss.png)

The loss functions are showed above, which is based on TD(0) learning.  

We start by measuring the performance of the Multi- Agent architecture on a simple stacking task. We choose this particular task because it is very useful for illustrating the key ideas of our algorithm, as it is natural to divide the original action space into type choosing and position choosing. In this experiment, our aim is to stack rectangular blocks of four different sizes together while making them as com- pact as possible and ending up with the lowest overall height possible. 

![](https://github.com/keqinw/keqinw.github.io/raw/master/images/stack_result.png)

Above is the result comparation in Stacking problem. The bumpiness is an indicator calculated by the variance of the outline (marked with blue line in the Figure), the smaller the number, the flatter the top layer of the pile. Obviously, within the same training episodes, DQN learned almost no reasonable policy; DDQN learned a good but still imperfect policy; and MAN learned an optimal policy, which outputs the lowest height and bumpiness.

We conduct a thorough examination of our suggested method on the Arcade Learning Environment (ALE), to confirm the capacity to tackle more complicated problems.  

From among 57 games in ALE, 12 games that combine button and joystick control with an action space of 18 were chosen. In DQN and DDQN where we use the original action space, we had difficulty mastering joystick and button control at the same time. Instead, using MAN, we can think differently, i.e., first determine the direction of joystick (9 actions in total), and then determine to press the button or not (2 actions in total). Thus, we reduce 18 actions to 11 (9+2) actions which needs less exploration theoretically. 

![](https://github.com/keqinw/keqinw.github.io/raw/master/images/avg_score.png)

Above figure shows the nomarlization scores of DQN, DDQN, and MAN. Our method boosted the average normalized score from 261% (with DQN) to 397.7%.
