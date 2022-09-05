---
title: "Late but Safe: Control Car Braking with Delay-Aware Reinforcement Learning"
permalink: /late/
author_profile: true
---
Real-world Autonomous Vehicle (AV) applications are susceptible to delays, whether caused by environmental changes, or hardware and software constraints. To ensure the safety of AV deployment, manufacturers need to create a system that is robust to delay. Our research aimed to evaluate the performance of Delay-Aware Trajectory Sampling Algorithm on AV applications.  

### Problem Definition
We assign a 1-dimensional vehicle to perform a braking task for our preliminary environment. A vehicle moving in a linear trajectory aims to stop within 0.3m around a pre-selected point.
* Point distance from start point (d) = 3m ≤ d ≤ 7m.
* Vehicle initial speed (vo) = 10m/s.
* Action = amount of force applied to the brake (a), range between -1 ≤ a ≤ 0 : a = -1 -> brake fully depressed; a=0 ->no forcegiven.
* We use PyBullet to design our OpenAI Gym simulation environment.
* We performed 100 simulations to determine: Success rate for each algorithm and Error between actual stop position and target point.

### Methods
DATS: Based on probabilistic ensembles with trajectory sampling (PETS), DATS is a new version whoose state vector is augmented with an action sequence being executed in the next n steps where n ∈ N is the delay duration.
![](https://github.com/keqinw/keqinw.github.io/raw/master/images/loss_dats.png)

### Result
<img src="https://github.com/keqinw/keqinw.github.io/raw/master/images/brake_delay.gif" height="250">
<img src="https://github.com/keqinw/keqinw.github.io/raw/master/images/brake-delay-MBRL-DATS.gif" height="250">
![](https://github.com/keqinw/keqinw.github.io/raw/master/images/result_dats.png)

DATS results outperformed other methods due to the data augmentation to obtain a better dynamic model. Instead of relying only on the state before n steps, DATS utilizes the information of the previous n steps and the following n actions to predict the current action. Specifically, the success rate raised from 24% (PETS) to 74% (DATS), and the average error distance decreased from 1.26m (PETS) to 0.34m (DATS).

