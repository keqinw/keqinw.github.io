---
title: "Parallel Robot System for Objects Sorting"
permalink: /parallel/
author_profile: true
---

We developed a new parallel robot and based on it, we designed an intelligent gripping system for disordered parts on the assembly line, making the process of gripping parts easy and efficient.  

The Bottom left figure shows the machine we built, which contains the following hardware modules: frame, parallel robot (internal DC power supply, MKS SBASE microcontroller, etc.), end gripper, conveyor belt, USB camera, LCD display, and some necessary auxiliary components and the host computer Raspberry Pi.  

![](https://github.com/keqinw/keqinw.github.io/raw/master/images/robot.png) 
![](https://github.com/keqinw/keqinw.github.io/raw/master/images/simu.png) 

We simulated curve of motor torque load in Simulink and estimated the action space with Monte Carlo for safety guarantee. The result (the bottom right figure) shows that our new design could dramatically decrease the load on motor, which is good for longer service life.


Finally, we applied the Parallel Robot System in a real-world assembly line, in which the robotic arm detects the position of the randomly placed objects and stacks them separately by color and type.  

![](https://github.com/keqinw/keqinw.github.io/raw/master/images/picking.gif) 

This project won the `Best Graduation Design` Prize among 100+ projects in Mechanical Engineering Department.



