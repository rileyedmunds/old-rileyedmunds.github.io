---
layout: post
title: Tensegrity Research
date: 2016-12-19 6:25:19
---


On December 15th, we concluded development of the TT4-Mini spherical tensegrity robot. Initially developed for planetary scouting, this smaller scale vehicle will be used as a test-bed for modeling robotic actuation and behavior across simulated planetary surfaces.



Here's what we built...

1. Controller

    - Built ergonomic physical controller, future-proofed for future development (space for additional control modes)
    - Integrated RF communication using XBee Wireless Modules in lieu of faulty Bluetooth connection.
    - Rewrote control software for increased efficiency and reliability, emphasizing code modularity in preparation for 'automatic' control mode. 

2. Tensegrirty Structure

    - Extended rod length from 10" to 12".
    - Designed new, sturdy motor covers.
    - Upgraded from plastic endcaps to metallic endcaps.
    - Designed and printed new spherical payload box structure.

3. Receiver

    - Refactored receiver code to efficiently parse and immediately execute motor commands received via RF.
    - Designed new PCB to fit within spherical payload box.
  
<br>

[See our robot in action! (YOUTUBE)](https://www.youtube.com/watch?v=1IZeTiKoyLw&vq=hd720){:target="_blank"}


![robot_side](https://raw.githubusercontent.com/rileyedmunds/rileyedmunds.github.io/master/images/tensegrity/sidetable.JPG)

Payload box PCB Schematics:

![pcb schematic](https://raw.githubusercontent.com/rileyedmunds/rileyedmunds.github.io/master/images/tensegrity/schematic.JPG)

Payload Box PCB:

![slave_pcb](https://raw.githubusercontent.com/rileyedmunds/rileyedmunds.github.io/master/images/tensegrity/pcb.JPG)

Physical controller prototype:

![controller prototype](https://raw.githubusercontent.com/rileyedmunds/rileyedmunds.github.io/master/images/tensegrity/controller.JPG)
    
    
Next semester I'm hoping to dive into development and testing of the 'automatic' control mode!

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
