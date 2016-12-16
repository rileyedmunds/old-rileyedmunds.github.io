---
layout: post
title: Tensegrity Research
date: 2016-12-09 9:25:14
---

Update:

The robot is complete! I will be posting more information soon.


---

Original Post: 

Beginning in August, I've been working in a [Robotics Lab](http://best.berkeley.edu/best-research/best-berkeley-emergent-space-tensegrities-robotics/). I spend ~8 hours/week working on control systems , software, and animations.

Here are a couple things I've been working on and thinking about:


1. Applying reinforcement learning.

Our lab's collaborators at NASA Ames have developed a [novel tweak on the guided policy search algorithm](https://arxiv.org/abs/1609.09049), that meshes localized decisions and global decisions to learn a gait for the tensegrity.

The algorithm processes a very limited feature set: while the researchers attempted to collect more data, they ended up using 12 accelerometer measurements from each rod. I would like to propose attaching IMUs to each rod for far more comprehensive measurements and more holistsic feature selection.

2. Incorporating vision.

As of this moment, the robot is controlled remotely by observing its current state and actuating motors according to which rods currently make up the base of the tensegrity and would most efficiently shift the center of mass ouside the base, and thus make the robot roll.

What if we could see in first person which rods form the base of the tensegrity? I propose including an fpv camera (within a gyroscope, to stay upright) within the payload box at the center of the robot. From there, we could write a simple image processing script to detect color-coded rods and thus infer which rods currently make up the base of the tensegrity.

For deployment of the robot in a real exploration scenario, first person vision seems necessary.

3. Distributing the nodes and relying on AI.

If reinforcement learning can in fact learn gait in a 24-node tensegrity, what's to say it can't solve gait in a 500-node tensegrity? 

Algorithms are often transferable, so once an optimization problem can be solved in one domain, its success in similar domains often requires little more than adjusted feature selection and tweaked settings. While this is clearly an oversimplification, I believe that solving and optimizing gait on one tensegrity opens the floodgates for research into other biologically-inspired robots that may consist of many more nodes.
