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

The loss function are showed above, which is based on TD(0) learning.
