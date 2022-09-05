---
title: "A DRL Framework Towards Drawing Single-stroked Handwriting Image"
permalink: /draw/
author_profile: true
---

We propose a reinforcement learning approach for automatically imitating a single-stroke painting
with a robotic manipulator.  

Directly learning a flat policy to solve the entire drawing task can be remarkably difficult due to the extremely long
task horizon. Therefore, we tackle this problem by decomposing it into a hierarchy of two sub-problems: a high-level
problem of learning an abstract-level CNN to generate instructions of where to move next step based on current state,
and a low-level problem that learning a PPO agent to control the manipulator move to the destination instructed by
high-level model. Concretely, the high-level is a typical supervised learning problem, which requires a specific dataset;
the low-level is a reinforcement learning problem, which trained by exploring the environment.  

![](https://github.com/keqinw/keqinw.github.io/raw/master/images/Slide3.png)

In addition, in order to accelerate the training, we utilized the Highsight Experience Replay (HER) and Goal Condition (GC). We add the goal into the state, and we transfer the detination of 80% experience by HER. 

However, the limitations of this framework are obvious. First, the control is open-loop, there is no feedback from motor or end-effect, which decrease the accuracy. Besides, this framework require us to train the CNN and PPO sperately, which is not end-to-end enough.  

Below is the result of the mimicry of various graphs. 

![](https://github.com/keqinw/keqinw.github.io/raw/master/images/experiment.png)

This is an application-oriented project, which helps me get familiar with the reinforcement learning, gym environment, stable-baseline etc.. 
