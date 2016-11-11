---
layout: post
title: Complex Sound
date: 2016-10-09 15:27:31
---

Beginning in August, I've been working in a [Robotics Lab](http://best.berkeley.edu/best-research/best-berkeley-emergent-space-tensegrities-robotics/). I spend ~8 hours/week working on control systems , software, and animations.

Here are a couple things I've been working on and thinking about:


1. Applying reinforcement learning.

> Our lab's collaborators at NASA Ames have developed a [novel tweak on the guided policy search algorithm](https://arxiv.org/abs/1609.09049), that meshes localized decisions and global decisions to learn a gait for the tensegrity.

The algorithm processes a very limited feature set: while the researchers attempted to collect more data, they ended up using 12 accelerometer measurements from each rod. I would like to propose attaching IMUs to each rod for far more comprehensive measurements and more holistsic feature selection.

2. Incorporating vision.

As of this moment, the robot is controlled remotely by observing its current state and actuating motors according to which

3. How do we plan on testing?

We're building a real-valued environmental sound classification CNN in Caffe, and a complex counterpart, with appropriate layer functions that pass complex data through the network. We will then run the two head-to-head, and aim to beat the real-valued network with the complex version.

I'd like to give a huge thank you to Stella Yu and Pat Virtue from the International Computer Science Institute (ICSI) for their counsel and advising during this project. You're both amazing researchers and inspiring mentors.
