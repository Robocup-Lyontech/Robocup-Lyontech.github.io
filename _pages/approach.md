---
permalink: /approach/
title: "Scientific approach for Robocup@home"
---


The architecture of LyonTech's embedded AI software is shown in Figure 3. It contains modules which have been developed in different research groups of the consortium, completed by ofthe shelf modules which tackle standard tasks, as well as engineering bricks interconnecting these modules. 
The scientic expertise of the consortium is broad and targets the needs of the competition:
Perception
Our computer vision experts bring knowledge in 
- gesture recognition [1], 
- activity recognition [2, 3]
- articulated pose estimation [4], 
- semantic segmentation [5]
- object recognition [6]. 

A large part of these methods are capable of running on real time and have been integrated in our platforms of mobile robots. Our combined work allows us to be aware of the objects present in a room, their locations, as well as the ongoing activities in this room.


## Motion planning and Decision making
Our expertise in robotics relates to motion planning in dynamic and uncertain environments, mapping, localization and decision-making for single and multi-robot systems. The work focuses on autonomous navigation in crowded environments (human-aware navigation) and in urban trac (autonomous vehicles) for human assistance [7{9]. We also explore robot and  cooperation for human scene observation [10], 3D environment mapping, transport and service delivery [11]. We experiment and evaluate the models with Pepper humanoids, fleets of mobile robots (cf. Figure 2) and UAVs, and two equipped/autonomous cars (see https://team.inria.fr/chroma/en/plate-formes/). 

## Human-Robot Interactions 
We have been working for years on different interactions with robots (from teleoperation to multirobots orchestration [12{
15]). Since this year, we also get strong support from the Hoomano company, which creates solutions for Human-Robot interaction in real world applications, in particular for Pepper robots.

## Integration 
All components are integrated using the ROS middleware, which is the base system of our robot. ROS oers the ability to connect a set of programs through synchronous and asynchronous communication. Moreover, by allowing a set of heterogeneous components (probes, actuators, services) to communicate in a normalized way, processing program can be reused. The **naoqi sdk**, provided by **softbank/aldebaran** with the **Pepper robot**, gives a set of API that is mainly used for Robot and Human interactions (speech recognition, text to speech, robot behavior feedbacks). In order to highlight the robot activity, the Pepper tablet gives visual feedbacks (javascript framework).

We define five principal functionality blocks in our architecture (gure 3).
The Robot Navigation Manager is in charge of localizing the robot and
allowing dynamic navigation (obstacles avoidance). The analysis of the robot
environment is performed by Object Detection and recognition modules,
mainly deep neural networks developed inhouse [6] or o-the-shelf modules
like YOLO 9000 [16]. Labeled object positions are provided to other blocks.
All human robot interactions are managed by the Robot Human interaction
block embedded in the robot. The robot also maintains a knowledge database
about its environment (humans, objects and points of interest positions).

Finally, the general manager block works like an orchestrator and gives order
to other blocks in order to achieve scenarios.
