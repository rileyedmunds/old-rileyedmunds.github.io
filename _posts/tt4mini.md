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

As of this moment, the robot is controlled remotely by observing its current state and actuating motors according to which rods currently make up the base of the tensegrity and would most efficiently shift the center of mass ouside the base, and thus make the robot roll.

What is we could see in first person which rods form the base of the tensegrity? I propose including an fpv camera (within a gyroscope, to stay upright) within the payload box at the center of the robot. From there, we could write a simple image processing script to detect color-coded rods and thus infer which rods currently make up the base.

Furthermore, for real planetary exploration, this feature is clearly mandatory.
