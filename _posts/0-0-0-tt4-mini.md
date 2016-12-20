---
layout: post
title: Tensegrity Research
date: 2016-12-09 9:25:14
---

Update:

The robot is complete! I will be posting more information soon.


Upgrades since last TT4-Mini release:

1. Controller

    - Build ergonomic physical controller, future-proofed for future development (space for additional control modes)
    - Integrated RF communication using XBee Wireless Modules in lieu of faulty bluetooth connection.
    - Rewrote control software for increased efficiency and reliability, emphasizing code modularity in preparation for automatic control mode. 

2. Tensegrirty Structure

    - Extended rod length from 10" to 12".
    - Designed new motor covers.
    - Upgraded from plastic endcaps to metallic endcaps.
    - Designed and printed new spherical payload box structure.

3. The slave PCB within the tesnsegrity structure

    - Refactored slave code to efficiently parse and execute RF motor commands.
    - Designed new PCB to fit within spherical payload box.


See our robot in action!

[YOUTUBE VIDEO DEMO](https://www.youtube.com/watch?v=vTpg6qIS8t8&vq=hd720)


![robot_top](https://raw.githubusercontent.com/rileyedmunds/rileyedmunds.github.io/master/images/tensegrity/table.JPG)

![robot_side](https://raw.githubusercontent.com/rileyedmunds/rileyedmunds.github.io/master/images/tensegrity/sidetable.JPG)

![pcb schematic](https://raw.githubusercontent.com/rileyedmunds/rileyedmunds.github.io/master/images/tensegrity/schematic.JPG)

![slave_pcb](https://raw.githubusercontent.com/rileyedmunds/rileyedmunds.github.io/master/images/tensegrity/pcb.JPG)

![controller prototype](https://raw.githubusercontent.com/rileyedmunds/rileyedmunds.github.io/master/images/tensegrity/controller.JPG)

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
